<template>
  <div
    class="cursor-pointer w-[200px] border border-gray-300 rounded-md text-center py-3 my-4 mx-auto"
    @click="closeWindow"
  >
    閉じる
  </div>
</template>
<script setup>
const emit = defineEmits(["closeWindow"]);

const closeWindow = () => {
  emit("closeWindow");
};
</script>
