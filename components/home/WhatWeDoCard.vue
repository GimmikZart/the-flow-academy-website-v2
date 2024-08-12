<script setup>
const props = defineProps({
    image: {
        type: String,
        required: true,
    },
    title: {
        type: String,
        required: true,
    },
    description: {
        type: String,
        required: true,
    }
})

</script>
<template>
    <div class="flex flex-col gap-3 border-b pb-10">
        <NuxtImg :src="image" alt="image" class="h-[150px] w-full object-cover rounded-xl" />
        <div class="border-x-4 p-3 border-orange-500/50 flex flex-col gap-3">
            <h2 class="text-4xl text-orange-500 font-bold">{{title}}</h2>
            <p v-html="description" />
        </div>
    </div>
</template>