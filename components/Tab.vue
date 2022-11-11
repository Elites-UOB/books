<template>
    <div class="cursor-pointer text-center text-xs min-w-[40px] font-medium px-[8px] py-[4px]" :class="[
        active
        ? 'text-white'
        : 'text-[#717171] bg-transparent',

        'text-white'
    ]">
        <slot />
    </div>
</template>

<script setup>
const props = defineProps({
    active: {
        type: Boolean,
        default: false,
    }
})
</script>
