<template>
  <main class="w-60 mx-auto my-8">
    <section
      class="border-double border-4 border-red-500 text-center text-red-500"
    >
      <h1 class="border-b-2 border-red-500 py-2">今日の運勢</h1>
      <p class="font-bold text-3xl py-6">{{ result }}</p>
    </section>
    <Button btnName="おみくじを引く" @clickBtn="clickBtn"></Button>
  </main>
</template>
<script setup lang="ts">
const result = ref("?");
const clickBtn = () => {
  const results = ref(["大吉", "中吉", "小吉", "凶"]);
  const n = ref(Math.floor(Math.random() * results.value.length));
  result.value = results.value[n.value];
};
</script>
