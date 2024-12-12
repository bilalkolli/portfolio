<template>
    <div class="Projets" id="Projets">
        <h4>Mes projets</h4>
        <span>Une liste de projets Open Source que je maintiens ou sur lesquels je contribue.</span>
        <hr>
        <NuxtLink to="https://quiznuxt.netlify.app/" target="_blank" class="projet1">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" stroke="rgb(0 153 242/1)" viewBox="0 0 24 24" aria-hidden="true"><path d="M22 19a2 2 0 0 1-2 2H4a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h5l2 3h9a2 2 0 0 1 2 2z"></path></svg>
            <p class="nameproject">QuizNuxt</p>
            <p>Fullstack project called QuizNuxt built with Nuxtjs, Vuejs, Prisma, Javascript, supabase, and hosted on Vercel</p>
            <p>Nuxtjs • Vuejs • Javascript • Prisma</p>
        </NuxtLink>
    </div>
</template>
    
<style scoped>
.Projets{
    height: 60vh;
    display: flex;
    flex-direction: column
}
span {
    padding-bottom: 2rem;
    opacity: 0.7
}
h4 {
    font-size: 50px;
    padding-bottom: 1.5rem;
    font-weight: 800;
    letter-spacing: -0.5px
}
hr {
    width: 100%;
    margin-bottom: 2%
}
.projet1 {
    max-width: 500px;
    padding: 30px 20px;
    min-height: 250px;
    border: 2px solid rgb(64 64 64/ 1);
    border-radius: 5px
}
.projet1:hover {
    border-color: rgb(0 153 242/1)
}
svg {
    width: 40px
}
.nameproject {
    font-weight: 700;
    font-size: 24px;
    opacity: 1
}
p {
    opacity: 0.7;
    margin-top: 13px
}
@media only screen and (max-width: 948px) {
    .Projets {
        padding-top: 50px;
}
}
@media only screen and (max-width: 567px) {
    .Projets {
        margin: 10px;
        justify-content: center;
        text-align: center;
        align-items: center
    }
    .projet1 {
        margin: 10px 15px;
    }
}
@media only screen and (max-width: 394px) {
    .projet1 {
        min-height: 330px
    }
}
</style>
