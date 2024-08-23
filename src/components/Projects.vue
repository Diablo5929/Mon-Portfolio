<script setup>
    import { ref } from 'vue'
    import { projects } from '@/data/project.json';

    import TitreNiveau2 from './TitreNiveau2.vue';
    import SmallCard from './Project_SmallCard.vue';
    import Modal from './Modal.vue';

    let showModal = ref( false ) 
    let msgToModal = ref('')
</script>

<template>
    <div id="projets">
        <div class="projets__title">
            <TitreNiveau2>Projets</TitreNiveau2>
        </div>

        <div class="smallCard__box">
            <SmallCard @click="showModal=true; msgToModal=i" v-for="i in projects" :projet="i"></SmallCard>
        </div>
        <Modal v-if="showModal" @close="showModal = false" :projet="msgToModal"></Modal>
    </div>
</template>

<style scoped>
    button {
        border: none;
        background-color: greenyellow;
    }

    #projets {
        background-color: black;
        padding: 15px 0px;
        border-top: 3px solid greenyellow;
        left: 0px;
        right: 0px;
    }

    .material-symbols-outlined {
        font-size: 2em;
    }

    .projets__title {
        display: flex;
        align-items: start;
        gap: 5px;
        justify-content: center;
    }

    .smallCard__box {
        margin: 20px auto;
        width: 60%;
        display: flex;
        gap: 25px;
        align-items: center;
        justify-content: center;
        flex-wrap: wrap;
    }

    .SmallCard {
        flex-basis: 30%;
        max-width: 270px;
        min-width: 270px;
    }
</style>