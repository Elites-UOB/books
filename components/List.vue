<template>
    <div class="border-2 border-[#262626] rounded flex justify-center w-min mr-4" :class="{ 'flex-col w-96' : col }">
        <slot />
    </div>
</template>

<script setup>
const props = defineProps({
    col: {
        type: Boolean,
        default: false,
    }
})
</script>
