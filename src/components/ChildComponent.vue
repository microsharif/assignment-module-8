<script setup>
    defineProps(['message']);
    defineEmits(['messageEmitted'])
</script>

<template>
    <div class="p-4 mb-2 bg-[#faeaeb] rounded border border-slate-700">
        <h2 class="mb-3 underline font-semibold text-lg">Child Component</h2>
        <p class="text-base mb-3">{{ message }}</p>
        <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded" @click="$emit('messageEmitted', 'Hello World from child componet')">Send Message to Parent</button>
    </div>
</template>

<style scoped></style>