<template>
  <div
    class="cursor-pointer w-[200px] border border-gray-300 rounded-md text-center py-3 my-4 mx-auto"
    @click="openWindow"
  >
    詳細を見る
  </div>
</template>

<script setup>
const emit = defineEmits(["openWindow"]);
const props = defineProps([""]);
const openWindow = () => {
  emit("openWindow");
};
</script>
