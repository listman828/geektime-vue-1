<template>
  <li class="item_class">
    <input type="checkbox" v-model="checked">
    <slot name="itemName" v-bind="{checked}"></slot>
  </li>
</template>

<script>
export default {
  name: "TodoItem",
  props: ["item"],
  data() {
    return {
      checked: false
    };
  }
};
</script>

<style scoped>
.item_class {
  color: red;
}
</style>


