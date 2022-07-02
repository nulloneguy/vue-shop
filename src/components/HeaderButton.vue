<script setup lang="ts">
const props = defineProps({
    title: { type: String, required: true },
    icon: { type: String, required: false },
})
</script>

<template>
  <a class="px-3 py-2 inline-block text-center shadow-sm border border-gray-200 rounded-md hover:bg-gray-100 hover:border-gray-300 flex items-center" href="#">
    <div v-if="props.icon" :i="props.icon" class="text-gray-400" />
		<span class="hidden lg:inline ml-1">{{ props.title }}</span>
	</a>
</template>
