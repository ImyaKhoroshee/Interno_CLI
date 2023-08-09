<template>
  <div class="pagination-button">
    <p class="pagination-button__text">01</p>
  </div>
  <div class="pagination-button">
    <p class="pagination-button__text">03</p>
  </div>
  <div class="pagination-button">
    <p class="pagination-button__text">04</p>
  </div>
  <div class="pagination-button">
    <svg
      width="9"
      height="16"
      viewBox="0 0 9 16"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        d="M1.55714 15L7.5 8.31429L1.55714 1.62857"
        stroke="#292F36"
        stroke-width="2"
        stroke-linecap="round"
        stroke-linejoin="round"
      />
    </svg>
  </div>
</template>

<script>
export default {
  name: "Pagination",
  props: {},
  components: {},
  data() {
    return {};
  },
};
</script>

<style scoped lang="scss">
.pagination-button {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 52px;
  height: 52px;
  border: 1px solid #cda274;
  border-radius: 50%;
  background-color: transparent;
  color: #292f36;
  font-family: Jost;
  font-size: 16px;
  font-style: normal;
  font-weight: 500;
  line-height: 150%;
  text-transform: capitalize;
  transition: 0.6s;
  &:hover {
    background-color: #f4f0ec;
    border: none;
  }
}
</style>
