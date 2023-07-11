<template>
  <div
    class="bg-black opacity-40 fixed left-0 right-0 bottom-0 top-0"
    v-show="!toggle"
    @click="closeWindow"
  ></div>
</template>

<style>
.hidden {
  display: none;
}
</style>

<script setup>
const emit = defineEmits(["closeWindow"]);
const props = defineProps(["toggle"]);
const closeWindow = () => {
  emit("closeWindow");
};
</script>
