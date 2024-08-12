<script setup>
const menuIsOpen = ref(false)

const routes = [
    {
        name: 'Home',
        to: '/',
        icon: 'ic:baseline-home'
    },
    {
        name: 'Corsi',
        to: '/corsi',
        icon: 'gravity-ui:target-dart'
    },
    {
        name: 'Insegnanti',
        to: '/insegnanti',
        icon: 'raphael:people'
    },
    {
        name: 'Percorsi',
        to: '/percorsi',
        icon: 'ph:path-bold'
    },
    {
        name: 'Extra',
        to: '/extra',
        icon: 'material-symbols:chip-extraction-rounded'
    },
    {
        name: 'Contatti',
        to: '/contatti',
        icon: 'material-symbols:contact-support-outline'
    },
]

</script>
<template>
    <header class="fixed bottom-0 left-0 w-full flex flex-col">
        <!-- MENU -->
        <section v-if="menuIsOpen" class="w-full bg-black/50 backdrop:blur-3 p-10 grid grid-cols-3 gap-2">
            <NuxtLink v-for="(route, idx) in routes" :key="idx" :to="route.to" class="p-3 border-2 flex flex-col items-center justify-center">
                <Icon :name="route.icon" class="text-white w-full h-auto aspect-square"/>
                <p class="text-white text-center">{{ route.name }}</p>
            </NuxtLink>
        </section>
        <!-- BOTTOM BAR -->
        <section class="p-3 bg-black w-full flex items-center justify-between">
            <div class="text-white">
                THE FLOW
            </div>
            <Icon v-if="!menuIsOpen" name="ci:hamburger-lg" class="text-white w-5 h-5" @click="menuIsOpen = true"/>
            <Icon v-else name="ic:outline-close" class="text-white w-5 h-5" @click="menuIsOpen = false"/>
        </section>
    </header>
</template>