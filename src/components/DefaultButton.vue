<template>
  <button
    class="default-btn"
    @click="onClick"
    :class="iconName !== '' ? 'with-icon' : ''"
  >
    <slot>Click me!</slot>
    <b-icon class="btn-icon" v-if="iconName !== ''" :icon="iconName"></b-icon>
  </button>
</template>

<script>
export default {
  name: "default-button",
  props: {
    iconName: {
      type: String,
      default: ""
    },
    onClick: {
      type: Function,
      required: true
    }
  },
  components: {}
};
</script>
<style lang="scss" scoped>
.default-btn {
  color: white;
  background: $secondary;
  border-radius: 25px;
  font-size: 18px;
  padding: 10px 45px;
  border: 0;
  position: relative;
  width: auto;
  &:focus {
    outline: 0;
  }
  &.with-icon .btn-icon {
    font-weight: 400;
    position: absolute;
    left: 80%;
    top: 25%;
    right: 5%;
    bottom: 0;
    display: none;
  }
  &:hover {
    background: darken($secondary, 10);
    transition: all 0.5s;
    box-shadow: 0 6px 15px darken($secondary, 20);
    &.with-icon {
      padding-right: 3.5rem;
      &.with-icon .btn-icon {
        display: inline;
        transition: all 0.3s;
      }
    }
  }
}
</style>
