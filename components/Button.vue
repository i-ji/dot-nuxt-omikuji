<template>
  <button
    class="w-full bg-red-500 rounded-lg text-white py-2 mt-4 hover:opacity-80 shadow-[0_4px_#7a0000] active:shadow-[0_1px_#7a0000] active:translate-y-[3px]"
    @click="clickBtn"
  >
    {{ btnName }}
  </button>
</template>
<script setup lang="ts">
const props = defineProps(["btnName"]);
const emit = defineEmits(["clickBtn"]);
const clickBtn = () => {
  emit("clickBtn");
};
</script>
