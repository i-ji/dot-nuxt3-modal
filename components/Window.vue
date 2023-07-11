<template>
  <section
    class="bg-white w-[300px] p-5 rounded-md absolute top-10 right-0 left-0 mx-auto"
    v-show="!toggle"
  >
    <p class="mb-5">
      こんにちは。こんにちは。こんにちは。こんにちは。こんにちは。こんにちは。こんにちは。こんにちは。こんにちは。こんにちは。
    </p>
    <Close @closeWindow="closeWindow" />
  </section>
</template>

<style>
/* .hidden {
  transform: translateY(-500px);
} */
</style>

<script setup>
const props = defineProps(["toggle"]);
const emit = defineEmits(["closeWindow"]);
const closeWindow = () => {
  emit("closeWindow");
};
</script>
