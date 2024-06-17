<template>
    <div class="hero">
        <div class="description">
            <h1>Développeur web front-end Vuejs 👋</h1>
            <h2>Je m'appelle Bilal Kolli. Un développeur web front-end avec le framework Vuejs !</h2>
            <NuxtLink :to="réseau.profile" class="liens" target="_blank" v-for="réseau in Réseaux_sociaux">
                <img width="45px" alt="image de réseaux social ou j'ai un profil disponible" :srcset="`${réseau.logo}`">
            </NuxtLink>
        </div>
        <div class="imagehero"></div>
    </div>
</template>

<script setup>
const Réseaux_sociaux = [
    { nom: "GitHub",profile:"https://github.com/bilalkolli",logo:"github.svg"},
    { nom: "Linkedin",profile:"https://www.linkedin.com/in/bilal-kolli/",logo:"Linkedin.svg"}
]
</script>

<style scoped>
.hero {
    display: flex;
    justify-content: center;
    height: 75vh;
    align-items: center
}
.description {
    max-width: 430px;
    margin-right: 100px
}
.logo {
    align-self: center
}
h1 {
    font-size: 40px;
    letter-spacing: -0.5px
}
h2 {
    margin: 20px 0px;
    font-size: 18px;
    opacity: 0.8;
    font-weight: 400;
    letter-spacing: -0.5px;
    line-height: 1.5em
}
p {
    font-size: 30px;
    font-weight: 700;
    margin-bottom: 20px;
    opacity: 0.8;
    width: 500px
}
a {
    margin-right: 10px
}
.imagehero {
    border-radius: 200em;
    height: 380px;
    width: 400px;
    animation: morph 8s ease-in-out infinite;
    border: 2px solid white;
    background-image: url('/public/photohero.webp')
} 

@keyframes morph {
    0% {
    border-radius: 60% 40% 30% 70% / 60% 30% 70% 40%
}
50% {
    border-radius: 30% 60% 70% 40% / 50% 60% 30% 60%
}
100% {
    border-radius: 60% 40% 30% 70% / 60% 30% 70% 40%
}
}

@media only screen and (max-width: 947px) {
    .hero{
        flex-direction: column-reverse
    }
    .description {
        text-align: center;
        margin-right: 0px
    }
    .imagehero {
        height: 600px
    }
}
@media only screen and (max-width: 505px) {
    .description {
        padding: 7px
    }
    .imagehero {
        height: 300px;
        width: 250px;
        background-position: 45% 25%
    }
}
@media only screen and (max-width: 431px) {
    h1 {
        font-size: 35px
    }
}
</style>