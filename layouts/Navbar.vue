<template>
    <div class="navbar">
        <p>Bilal KOLLI</p>
        <nav>
            <NuxtLink :to="`#${Categorie}`" class="ancres" v-for="Categorie in Categories">
                {{ Categorie }}
            </NuxtLink>
        </nav>
    </div>
</template>

<script setup>
const Categories = ["À propos","Projets","Contact"]
</script>

<style scoped>
.navbar {
    margin: 30px 10px;
    display: flex;
    justify-content: space-between
}
p {
    font-weight: 700;
    font-size: 18px
}
.ancres {
    margin-left: 50px
}
.ancres:hover {
    border-bottom: 1.5px solid white
}
@media only screen and (max-width: 513px) {
    nav {
        display: none
    }
    .navbar {
        margin-top: 5px
    }
}
</style>