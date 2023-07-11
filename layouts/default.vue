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
.fade-enter-active .fade-leave-active {
  transition: all 0.4s;
}

.fade-leave-to .fade-enter-from {
  opacity: 0;
  transform: translateY(-500px);
}
</style>

<script setup>
useHead({
  title: "Modal Window",
});

import { ref } from "vue";
const toggle = ref(true);

const openWindow = () => {
  toggle.value = false;
};

const closeWindow = () => {
  toggle.value = true;
};
</script>
