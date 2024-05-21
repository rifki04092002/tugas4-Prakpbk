<!-- ParentComponent.vue -->
<template>
  <div class="parent-component">
    <h2 style="color: blue">Parent Component</h2>
    <PinkChildComponent @childData="handleChildData" />
    <SlotComponent>
      <template v-slot:default>
        <p>Data pada slot: {{ slotData }}</p>
      </template>
    </SlotComponent>
    <p>Nama Saya: {{ childData }}</p>
  </div>
</template>

<script>
import PinkChildComponent from "./components/PinkChildComponent.vue";
import SlotComponent from "./components/SlotComponent.vue";

export default {
  components: {
    PinkChildComponent,
    SlotComponent,
  },
  data() {
    return {
      childData: "",
      slotData: "Component",
    };
  },
  methods: {
    handleChildData(data) {
      this.childData = data;
    },
  },
};
</script>

<style scoped>
.parent-component {
  background-color: #09ef3b;
  padding: 20px;
  border-radius: 8px;
}
</style>
