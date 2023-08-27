<template>
  <div class="slider-item">
    <img :src="image.src" />
    <slot />
  </div>
</template>

<script>
export default {
  name: "SliderImage",
  props: {
    image: Object,
  },
  components: {},
  data() {
    return {};
  },
};
</script>

<style scoped lang="scss"></style>
