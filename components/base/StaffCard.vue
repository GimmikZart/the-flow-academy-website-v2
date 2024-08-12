<script setup>
const props = defineProps({
    image: {
        type: String,
        required: true,
    },
    name: {
        type: String,
        required: true,
    },
    roles: {
        type: Array,
        required: true,
    },
    color: {
        type: String,
        default: '#0000'
    }
})

const rolesFormatted = computed(() => {
    return props.roles.join(' | ')
})

const backgroundColor = computed(() => {
    return {
        backgroundColor: props.color
    }
})
</script>
<template>
    <div class="border-4 border-black aspect-square w-full -skew-x-3 relative" :style="backgroundColor">
        <NuxtImg :src="image" alt="staff" class="h-full w-full object-cover skew-x-3 absolute"/>
        <div class=" bg-black/50 w-full pt-0 pb-5">
            <h1 class="text-white text-3xl skew-x-3 font-bold relative px-5 py-1" style="z-index: 100">{{name}}</h1>
        </div>
        <div class="absolute bottom-0 bg-black/70 w-full p-3">
            <h3 class="text-white skew-x-3 text-lg">{{rolesFormatted}}</h3>
        </div>
    </div>
</template>