<template>
    <div class="Contact" id="Contact">
        <h5>Contact</h5>
        <span>Ne soyez pas timide ! Contactez-moi !</span>
        <hr>
        <div class="Contacts">
            <NuxtLink :to="contact.link" target="_blank" v-for="contact in contacts">
                {{ contact.name }}
            </NuxtLink>
        </div>
    </div>
</template>

<script setup>
const contacts = [
    {name:'kolli@mail.fr',link:'mailto:kolli@mail.fr'},
    {name:'bilalkolli@github',link:'https://github.com/bilalkolli'},
    {name:'bilalkolli@linkedin',link:'https://www.linkedin.com/in/bilal-kolli/'}
]
</script>

<style scoped>
.Contact{
    height: 50vh;
    display: flex;
    flex-direction: column
}
span {
    padding-bottom: 2rem;
    opacity: 0.7
}
h5 {
    font-size: 50px;
    padding-bottom: 1.5rem;
    font-weight: 800;
    letter-spacing: -0.5px
}
hr {
    width: 100%;
    margin-bottom: 2%
}
.Contacts {
    display: flex;
    flex-direction: column;
}
a {
    font-size: 3rem;
    margin-top: 10px;
}
a:hover {
    color: rgb(0 153 242/1);
}
@media only screen and (max-width: 567px) {
    .Contact {
        margin: 10px;
        justify-content: center;
        text-align: center;
        align-items: center
    }
    .projet1 {
        margin: 10px 15px;
    }
}
@media only screen and (max-width: 420px) {
    a {
    font-size: 1.5rem;
}
}
</style>