<template>
  <div class="waxon_tm_about">
    <div class="container">
      <div
        class="positon-relative waxon_tm_main_title"
        v-scroll-reveal="{ delay: 40, distance: '30px' }"
      >
        <div class="title">
          <h3>Galería<span class="bg">Galería</span></h3>
        </div>
      </div>
      <div class="gallery">
        <div class="gallery-item" v-for="(image, i) in images" :key="i">
          <img class="gallery-image" :src="image.url" :alt="image.title" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      images: [
        {
          url: require("@/assets/img/gallery/1.jpeg"),
          title:
            "person writing in a notebook beside by an iPad, laptop, printed photos, spectacles, and a cup of coffee on a saucer",
        },
        {
          url: require("@/assets/img/gallery/2.jpg"),
          title:
            "person writing in a notebook beside by an iPad, laptop, printed photos, spectacles, and a cup of coffee on a saucer",
        },
        {
          url: require("@/assets/img/gallery/3.jpg"),
          title:
            "person writing in a notebook beside by an iPad, laptop, printed photos, spectacles, and a cup of coffee on a saucer",
        },
        {
          url: require("@/assets/img/gallery/4.jpeg"),
          title:
            "person writing in a notebook beside by an iPad, laptop, printed photos, spectacles, and a cup of coffee on a saucer",
        },
        {
          url: require("@/assets/img/gallery/5.jpg"),
          title:
            "person writing in a notebook beside by an iPad, laptop, printed photos, spectacles, and a cup of coffee on a saucer",
        },
        {
          url: require("@/assets/img/gallery/6.jpg"),
          title:
            "person writing in a notebook beside by an iPad, laptop, printed photos, spectacles, and a cup of coffee on a saucer",
        },
        {
          url: require("@/assets/img/gallery/7.jpg"),
          title:
            "person writing in a notebook beside by an iPad, laptop, printed photos, spectacles, and a cup of coffee on a saucer",
        },
        {
          url: require("@/assets/img/gallery/8.jpg"),
          title:
            "person writing in a notebook beside by an iPad, laptop, printed photos, spectacles, and a cup of coffee on a saucer",
        },
        {
          url: require("@/assets/img/gallery/9.jpg"),
          title:
            "person writing in a notebook beside by an iPad, laptop, printed photos, spectacles, and a cup of coffee on a saucer",
        },
        {
          url: require("@/assets/img/gallery/10.jpg"),
          title:
            "person writing in a notebook beside by an iPad, laptop, printed photos, spectacles, and a cup of coffee on a saucer",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
.gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  grid-gap: 20px;
  margin-top: 20px;
}
.gallery-image {
  display: block;
  width: 100%;
  height: 80%;
  object-fit: cover;
  transition: transform 400ms ease-in;
}

.gallery-image:hover {
  transform: scale(1.1);
}
.gallery-item span {
  line-height: normal;
  font-size: 11px;
  margin: 0;
  background: #646464;
  color: white;
  font-style: italic;
  padding: 5px;
  text-align: center;
}
</style>