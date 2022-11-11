<template>
    <div :class="{'flex flex-row gap-2' : col}">
        <List :col="col">
            <Tab :active="selected == index + 1" v-for="(tab, index) in tabs" :key="tab" @click="() => {selected = index + 1, $emit('selected', selected)}">
                {{ tab }}
            </Tab>
        </List>

        <Panels :col="col">
            <Panel>
                <slot :name="'tab-' + selected" />
            </Panel>
        </Panels>
    </div>
</template>

<script setup>
import { ref, watch } from 'vue'

const props = defineProps({
    tabs: {
        type: Array,
        required: true,
    },
    selected: {
        type: Number,
        default: 0,
    },
    col: {
        type: Boolean,
        default: false
    }
});

const selected = ref(props.selected + 1);

watch(() => props.selected, (val) => {
    selected.value = val;
});
</script>
