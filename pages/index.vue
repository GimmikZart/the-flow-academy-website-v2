<script setup>

const whatWeDo = [
    {
        image: 'images/streetdance.jpg',
        title: 'Street dance',
        description: '<b>Locking, Popping, Breaking, Hip-Hop, House, Dancehall, Afro e twerk.</b> <br>Questi sono alcuni corsi di <b>danza urbana</b> che potrai trovare qui da noi alla <b>THE FLOW Dance Academy</b>.<br>Con <b>62 premi</b> a livello nazionale e con la vincita del programma televisivo ICREW andato in onda su <b>Mediaset La5</b>, la The Flow Dance Academy e’ la realtà più importante della città di Parma. <br> Nella nostra struttura avrai la possibilità di conoscere a 360° queste discipline.'
    },
    {
        image: 'images/streetdance.jpg',
        title: 'Dance',
        description: '<b>La danza e’ arte.</b> <br>E’ il nostro essere a scegliere lo stile che più ci rappresenta. <br><b>Salsa</b>, <b>Bachata</b>, e <b>Kizomba</b> ti consentiranno di dare voce al tuo lato passionale. <br><b>Classico</b>, <b>Moderno</b> e <b>Contemporaneo</b> ti permetteranno di esprimere il tuo lato più elegante.'
    },
    {
        image: 'images/streetdance.jpg',
        title: 'Pole Dance & Danze Aeree',
        description: "La nostra <b>Pole Academy</b> è in continua crescita. <br>Un mix tra benessere <b>fisico</b> e <b>mentale</b> . <br>Senza che tu te ne accorga il tuo corpo si plasmerà tra <b>Potenziamento muscolare</b>, <b>esercizi di flessibilità</b> e tutte le fantastiche figure aeree che potrai imparare con questa disciplina. <br><b>Pole Dance</b>...danza col palo...ma da quest'anno anche <b>cerchio, corda e tessuti aerei</b> !!!"
    },
    {
        image: 'images/streetdance.jpg',
        title: 'Fitness',
        description: "<b>Mantenersi in forma non e’ mai stato così facile!</b> <br>Grazie ai diversi corsi presenti presso la nostra struttura, avrai la possibilità di scegliere che tipologia di allenamento preferisci: se vuoi sfogarti a ritmo di musica i nostri corsi di <b>Zumba</b>, <b>Circuit Training</b>, <b>Acrobatica</b>, <b>Verticalismo</b>, <b>Avviamento all'artistico</b> e <b>Kangoo Jumps</b>, fanno al caso tuo. <br>Se vuoi evadere e rilassare mente e corpo, <b>Yoga</b> e <b>Pilates</b> sono ciò di cui hai bisogno."
    }
]

const staff = [
    {
        image: 'images/staff/alex_castagnetti.png',
        name: 'Alex Castagnetti',
        roles: ['Presidente', 'Art Director'],
        color: "#d48b6a"
    },
    {
        image: 'images/staff/papa.png',
        name: 'Enrico Castagnetti',
        roles: ['Vice Presidente'],
        color: "#d48b6a"
    },
    {
        image: 'images/staff/gimmik.png',
        name: 'Gimmik',
        roles: ['Segretario', 'Web Developer'],
        color: "#d48b6a"
    },
    {
        image: 'images/staff/fabio_boss.png',
        name: 'Fabio Boss',
        roles: ['Consigliere'],
        color: "#d48b6a"
    },
    {
        image: 'images/staff/eddie.png',
        name: 'Eduard Scortanu',
        roles: ['Content Creator', 'Social Media'],
        color: "#d48b6a"
    },
    {
        image: 'images/staff/alex_botti.png',
        name: 'Alex Botti',
        roles: ['Fotografo'],
        color: "#d48b6a"
    },
    {
        image: 'images/staff/enrythm.png',
        name: 'Enrythm',
        roles: ['Music Producer'],
        color: "#d48b6a"
    },
    {
        image: 'images/staff/alex_castagnetti.png',
        name: 'Susanna Gallù',
        roles: ['Responsabile Aquisti'],
        color: "#d48b6a"
    },
]
</script>
<template>
    <div>
        <!-- JUMBOTRON -->
        <section class="h-screen w-full flex flex-col">
            <div class="w-full absolute top-0 p-5 text-center bg-black/70">
                <h1 class="text-lg text-white font-bold">WELLCOME </h1> 
                <h3 class="text-lg text-white">to</h3>
                <h1 class="text-3xl text-white font-bold">THE FLOW</h1>
            </div>
            <div class="h-full w-full">
                <NuxtImg src="gif/street-gif.gif" alt="jumbogif" class="h-full w-full object-cover" />
            </div>
        </section>
        <!-- CHI SIAMO -->
        <section class="p-3 flex flex-col gap-5">
            <h1 class="text-black text-3xl border-b-2 border-orange-500 font-bold">CHI SIAMO</h1>
            <p class="p-3 text-black">La The Flow Dance Academy è una realtà consolidata nel panorama della danza e del fitness a Parma. Grazie ai suoi numerosi corsi, attività e servizi, avrai la possibilità di apprendere, migliorare te stesso e superare i tuoi limiti, stringendo al contempo profondi rapporti umani sia con i soci che con il nostro staff, che sarà sempre a tua disposizione per rendere l'esperienza impeccabile.</p>
        </section>
        <!-- COSA FACCIAMO -->
        <section class="p-3 flex flex-col gap-5">
            <h1 class="text-black text-3xl border-b-2 border-orange-500 font-bold">COSA FACCIAMO</h1>
            <HomeWhatWeDoCard v-for="(item, idx) in whatWeDo" :key="idx" :image="item.image" :title="item.title" :description="item.description"/>
        </section>
        <!-- IL NOSTRO STAFF -->
        <section class="p-3 flex flex-col gap-5">
            <h1 class="text-black text-3xl border-b-2 border-orange-500 font-bold">IL NOSTRO STAFF</h1>
            <div class="grid grid-cols-1 gap-3 p-5">
                <BaseStaffCard v-for="(item, idx) in staff" :key="idx" :image="item.image" :name="item.name" :roles="item.roles" :color="item.color"/>
            </div>
        </section>
    </div>
</template>