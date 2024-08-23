<script setup>
    import TitreNiveau2 from './TitreNiveau2.vue';

    const parcours = {
        annee1: {
            ecole: 'OpenClasRoom',
            date: 'Avril 2023 -  Avril 2024',
            title: 'Technicien et maintenance informatique',
        },
        annee2: {
            ecole: 'Centre europeen de formation',
            date: ' Juin 2024 - En cours',
            title: 'Developpeur web et mobil',
            comment: "Diplôme de developpeur web et web Mobile ."
        },
    }
</script>

<template>
    <div class="courses">
        <div class="courses__title">

            <TitreNiveau2>Mon parcours</TitreNiveau2>
        </div>
    
        <div class="parcours">
            <div class="ecole" v-for="annee in parcours">
                <h3 class="ecole__title">{{ annee.ecole }}</h3>
                <h4 class="ecole__info">{{ annee.title }} <span class="separation">|</span> {{ annee.date }}</h4>
                <p class="ecole__comment">{{ annee.comment }}</p>
            </div>
        </div>
    </div>
</template>

<style scoped>
    .courses {
        background-color: black;
        width: 60%;
        display: flex;
        flex-direction: column;
        align-items: center;
        margin: auto;
    }

    .courses__title {
        text-align: center;
    }

    .material-symbols-outlined {
        font-size: 4em;
    }

    .ecole__title {
        font-size: 1.25em;
    }

    .ecole__info {
        font-size: 1.05em;
    }

    .separation {
        font-style: italic;
        color: greenyellow;
    }

    .ecole__comment {
        text-indent: 2em;
        text-align: justify;
    }

    .parcours {
        margin-top: 15px;
        display: flex;
        flex-direction: column-reverse;
        gap: 25px;
    }

    .ecole {
        padding: 15px;
        background-color: black;
        border-radius: 25px;
        box-shadow: -4px 5px 10px greenyellow;
    }

    @media screen and (max-width: 480px) {
        .courses {
            width: 85%;
        }
    }
</style>