<template>
  <main class="project-details-main">
    <IntroBackground class="project-details__background" />
    <article class="project-details__content center">
      <h2 class="project-details__heading">Minimal Look Bedrooms</h2>
      <p class="project-details__text">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquamsem vitae turpis
        dignissim maximus. Aliquam sollicitudin tellumassa, vbel maximus purus posuere in.
        Dojrices gravida dignissim. Praesent at nibh in mi fringilla mattis. Phasellus ut
        dolor odio. Aenean in the ipsum vel lectus bibendum commodo.
      </p>
      <p class="project-details__text">
        In nec sem suscipit, convallis leo vitae, lacinia nibh. Cras amet tellus lectus.
        Vivamus ipsum nunc, mattis quis nibh id, pellentesque arcu. Donec a pellentesque
        Cras erat enim, gravida non ante vitae,elequis convallis elit, in viverra felis.
        Donec ultrices tellus vitae iaculisvd porta. Proin tincidunt ligula id purus
        porttitor.
      </p>
    </article>
    <div class="slider center">
      <div class="slider__content">
        <div class="slider-wrapper">
          <SliderImage
            :image="image"
            v-for="image in sliderImages"
            :id="image.id"
            :key="image.id"
            :src="image.src"
            alt="bedroom"
            class="slider-image"
            ><img
              :data-id="image.id"
              class="slider-image__zoom"
              src="../assets/zoom-icon.png"
              alt="zoom-icon"
              @click="zoom()"
            />
          </SliderImage>
        </div>
      </div>
    </div>
    <div class="slider-pagination center">
      <SliderPagination />
      <SliderPagination />
      <SliderPagination />
    </div>
  </main>
</template>

<script>
import IntroBackground from "@/components/IntroBackground.vue";
import SliderImage from "@/components/SliderImage.vue";
import SliderPagination from "@/components/SliderPagination.vue";

export default {
  name: "ProjectDetailsView",
  components: {
    IntroBackground,
    SliderImage,
    SliderPagination,
  },
  data() {
    return {
      sliderImages: [
        { id: "slider-image_1", src: require("../assets/slider.jpg") },
        { id: "slider-image_2", src: require("../assets/slider2.jpg") },
        { id: "slider-image_3", src: require("../assets/slider3.jpg") },
      ],
    };
  },
  methods: {
    zoom() {},
  },
};
</script>

<style scoped lang="scss">
.project-details {
  &__background {
    background-image: url("../assets/backgroud-project-details.jpg");
    background-size: cover;
    display: flex;
    height: 364px;
  }
  &__content {
    padding-top: 200px;
    padding-left: 630px;
    padding-right: 611px;
  }
  &__heading {
    color: #292f36;
    font-family: DM Serif Display;
    font-size: 50px;
    font-style: normal;
    font-weight: 400;
    line-height: 125%;
    letter-spacing: 1px;
    margin-bottom: 8px;
  }
  &__text {
    color: #4d5053;
    font-family: Jost;
    font-size: 22px;
    font-style: normal;
    font-weight: 400;
    line-height: 33px;
    letter-spacing: 0.18px;
    margin-bottom: 36px;
  }
}
.slider {
  &__content {
    max-width: 1201px;
    overflow: hidden;
  }
  &-item {
    margin-top: 61px;
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  &-wrapper {
    display: flex;
    flex-direction: row;
    gap: 25px;
    transition: all 1s;
  }
  &-image__zoom {
    position: absolute;
    cursor: pointer;
    transition: 1s;
  }
  &-pagination {
    display: flex;
    flex-direction: row;
    gap: 15px;
    justify-content: center;
    padding-top: 15px;
    padding-bottom: 170px;
  }
}
.scale {
  transform: scale(1, 1);
}
</style>
