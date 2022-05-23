<template>
  <div class="fields">
    <ValidationObserver v-slot="{ handleSubmit }">
      <form class="contact_form" @submit.prevent="handleSubmit(onSubmit)">
        <div class="first">
          <ul>
            <ValidationProvider
              name="name"
              rules="required"
              v-slot="{ errors }"
            >
              <li>
                <input
                  v-model="email.subject"
                  type="text"
                  placeholder="Asunto"
                  autocomplete="off"
                  @keyup="onSubmit"
                />
                <span class="inpur-error">{{ errors[0] }}</span>
              </li>
            </ValidationProvider>

            <ValidationProvider
              name="email"
              rules="required|email"
              v-slot="{ errors }"
            >
              <li>
                <input
                  type="text"
                  rules="required|email"
                  v-model="email.cc"
                  placeholder="Email"
                  @keyup="onSubmit"
                />
                <span class="inpur-error">{{ errors[0] }}</span>
              </li>
            </ValidationProvider>
            <ValidationProvider
              name="message"
              rules="required"
              v-slot="{ errors }"
            >
              <li>
                <textarea
                  v-model="email.body"
                  placeholder="Mensaje"
                  @keyup="onSubmit"
                ></textarea>
                <span class="inpur-error">{{ errors[0] }}</span>
              </li>
            </ValidationProvider>
          </ul>
        </div>
        <div class="tokyo_tm_button">
          <a :href="outputUrl" class="ib-button">Enviar</a>
        </div>
      </form>
    </ValidationObserver>
  </div>
</template>

<script>
import { ValidationObserver } from "vee-validate";
import { ValidationProvider } from "vee-validate/dist/vee-validate.full.esm";
export default {
  components: {
    ValidationObserver,
    ValidationProvider,
  },
  data() {
    return {
      email: {
        subject: "",
        cc: "",
        body: "",
      },
      mailHost: "yesidvh@gmail.com",
      outputUrl: "Type something",
    };
  },
  created() {
    this.onSubmit();
  },
  methods: {
    onSubmit() {
      this.outputUrl = "mailto:" + this.mailHost;
      const emailKeys = Object.keys(this.email);
      const remaining = emailKeys.filter(
        (key) => this.email[key].trim().length > 0
      );
      if (remaining.length > 0) {
        this.outputUrl += "?";
      }
      this.outputUrl += remaining
        .map((key) => `${key}=${encodeURI(this.email[key].trim())}`)
        .join("&");
    },
  },
};
</script>

<style lang="scss">
.inpur-error {
  color: red;
  font-size: 14px;
  padding-top: 5px;
}
</style>
