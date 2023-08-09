<template>
  <main class="main">
    <section class="banner-error">
      <Banner
        v-for="banner in errorBanner"
        :banner="banner"
        :buttonText="errorButtonText"
      />
    </section>
  </main>
</template>

<script>
import Banner from "@/components/Banner.vue";

export default {
  name: "404View",
  components: {
    Banner,
  },
  data() {
    return {
      errorButtonText: "Back To Home",
      errorBanner: [
        {
          id: "errorbanner",
          src: require("../assets/bannererror.jpg"),
          alt: "destroyed-flat",
          heading: "404",
          paragraph: "We are sorry, but the page you requested was not found",
          link: "/",
        },
      ],
    };
  },
};
</script>
<style scoped lang="scss">
.banner-error {
  max-width: 1920px;
  margin: 0 auto;
  padding-left: 360px;
  padding-bottom: 100px;
}
.banner-error :deep(.banner-box) {
  display: flex;
  flex-direction: row-reverse;
  gap: 81px;
}

.banner-error :deep(.banner__text) {
  padding-top: 272px;
}
.banner-error :deep(.banner__image) {
  border-bottom-left-radius: 37%;
}
.banner-error :deep(.banner__heading) {
  color: #cda274;
  font-family: DM Serif Display;
  font-size: 250px;
  font-style: normal;
  font-weight: 400;
  line-height: 97%;
}
.banner-error :deep(.banner__paragraph) {
  margin-bottom: 41px;
  color: #292f36;
  font-family: DM Serif Display;
  font-size: 35px;
  font-style: normal;
  font-weight: 400;
  letter-spacing: 0.35px;
  line-height: 51px;
}
</style>
