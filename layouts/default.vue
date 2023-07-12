<template>
  <div class="text-sm">
    <Open @openWindow="openWindow" />

    <Mask @closeWindow="closeWindow" :toggle="toggle" />
    <transition name="fade">
      <Window @closeWindow="closeWindow" :toggle="toggle" />
    </transition>
  </div>
</template>

<style>
.fade-enter-active,
.fade-leave-active {
  transition: transform 0.4s;
}

.fade-enter-from,
.fade-leave-to {
  transform: translateY(-500px);
}
</style>

<script setup>
useHead({
  title: "Modal Window",
});

import { ref } from "vue";
const toggle = ref(true);
const show = ref(true);

const openWindow = () => {
  toggle.value = false;
};

const closeWindow = () => {
  toggle.value = true;
};
</script>
