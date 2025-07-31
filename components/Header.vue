<script setup lang="ts">
const props = defineProps(["subtitle"]);
</script>

<template>
  <div class="flex flex-col gap-1 border-b-2 border-[#990000] px-1 pb-2 mb-2">
    <div class="text-lg font-bold">{{ props.subtitle || "&nbsp;" }}</div>
    <div class="text-3xl font-bold">
      <slot />
    </div>
  </div>
</template>
