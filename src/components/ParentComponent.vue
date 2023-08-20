<script setup>
    import { ref } from 'vue';
    import ChildComponent from './ChildComponent.vue';

    const childMessage = ref('')
    const message = ref('Hello world from parent component')
    const handleMessageEmitted = (msg) => {
        childMessage.value = msg
    }
</script>

<template>
    <div class="p-4 mb-2 bg-[#faeaeb] rounded border border-slate-700">
        <h2 class="mb-3 underline font-semibold text-lg">Parent Component</h2>
        <p class="text-base">{{ childMessage }}</p>
    </div>
    <ChildComponent :message = "message" @messageEmitted = "handleMessageEmitted"></ChildComponent>
</template>

<style scoped></style>