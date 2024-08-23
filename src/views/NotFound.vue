<script setup>
    import TitreNiveau2 from '@/components/TitreNiveau2.vue';
</script>

<template>
    <div>
        <RouterLink class="error404" to="/">
            <TitreNiveau2 class="title">ERROR-404</TitreNiveau2>
            <p class="CTA">Revenir sur le site</p>
        </RouterLink>
    </div>
</template>

<style scoped>
    div{
        margin: 15px;
        background-color: black;
    }

    .error404 {
        background-origin: content-box;
        background-repeat: no-repeat;
        background-position: center;
        background-size: cover;
        width: 80%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-evenly;
        gap: 2em;
        padding: 15vh 0;
        margin: auto;
        text-decoration: none;
        border-radius: 15%;
        box-shadow: -4px 4px 25px greenyellow;
    }

    img {
        width: 50%;
        height: auto;
        border-radius: 35%;
        box-shadow: -4px 4px 25px #060640;
    }

    .title {
        font-size: 2em;
    }

    @media screen and (max-width: 480px) {
        .error404 {
            width: 100%;
            padding: 5vh 0;
            margin-top: 25%;
        }
    }
</style>