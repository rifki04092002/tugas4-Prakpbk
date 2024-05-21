<!-- PinkChildComponent.vue -->
<template>
  <div class="child-component">
    <h3 style="color: blue">Child Component</h3>
    <button @click="sendDataToParent">Ngirim Data</button>
  </div>
</template>

<script>
export default {
  methods: {
    sendDataToParent() {
      this.$emit("childData", "RIFKI NUL ARIF PALING KECE");
    },
  },
};
</script>

<style scoped>
.child-component {
  background-color: yellowgreen;
  padding: 10px;
  border-radius: 5px;
}

/* Menentukan warna teks untuk komponen anak */
.child-component h3 {
  color: rgb(46, 39, 39); /* Warna teks hitam */
}
</style>
