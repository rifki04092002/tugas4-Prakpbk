<!-- SlotComponent.vue -->
<template>
  <div class="slot-component">
    <h3 style="color: blue">Slot Component</h3>
    <slot></slot>
  </div>
</template>

<script>
export default {
  data() {
    return {
      slotData: "Data pada slot component",
    };
  },
};
</script>

<style scoped>
.slot-component {
  background-color: yellow;
  padding: 10px;
  border-radius: 5px;
}
</style>
