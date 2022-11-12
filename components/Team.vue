<template>
    <div grid="~ cols-3 gap-10">
        <div v-for="person in team" :key="person.name" flex="~ col gap-2">
            <span>{{person.job}}</span>
            <span text="2xl">{{person.name}}</span>
            <a v-if="person.website" class="text-lg" :href="person.website">{{person.website}}</a>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue'
const props = defineProps(['src'])
const team = ref([])

fetch(`/pages/${props.src}/team.json`).then(res => res.json().then(data => team.value = data))
</script>