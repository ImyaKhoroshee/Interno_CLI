<template>
  <main class="main">
    <section class="banner">
      <Intro
        v-for="banner in errorBanner"
        :banner="banner"
        :key="banner.id"
        :src="banner.src"
        :alt="banner.alt"
        :heading="banner.heading"
        :paragraph="banner.paragraph"
        :buttonText="errorButtonText"
      />
    </section>
  </main>
</template>

<script>
import Intro from "@/components/Intro.vue";

export default {
  name: "404View",
  components: {
    Intro,
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
        },
      ],
    };
  },
};
</script>
<style scoped lang="scss">
// .banner__button {
//   display: flex;
//   padding: 23px 47px 24px 48px;
//   flex-direction: row;
//   align-items: center;
//   gap: 7px;
//   border: none;
//   border-radius: 18px;
//   background: #292f36;
//   box-shadow: 0px 10px 20px 0px rgba(192, 192, 192, 0.35);
//   transition: 0.3s;
//   &:hover {
//     background: #cda274;
//   }
// }
// .banner__button-link {
//   color: #fff;
//   text-align: center;
//   font-family: Jost;
//   font-size: 18px;
//   font-style: normal;
//   font-weight: 600;
//   letter-spacing: 1.25px;
// }

// .banner__button:hover .banner__button-svg path {
//   transition: 0.3s;
//   stroke: #292f36;
// }
</style>
