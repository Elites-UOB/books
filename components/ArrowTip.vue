<template>
    <div display="inline" w="full" bg="gray-200" dir="ltr" relative="~">
        <slot />

        <div flex="~" w="full" left="0" bottom="0" absolute="~">
            <span w="full" h="2px" bg="gray-500"></span>
        </div>
    </div>
</template>

<script setup>
const props = defineProps(['position'])
</script>