<script setup>
    import TitreNiveau2 from './TitreNiveau2.vue';

    const parcours = {
        annee1: {
            entreprise: 'Policier-adjoint commissariat de Roubaix',
            date: '03 Août 2015 - 01 Décembre 2022',
            title: 'Police Secour',
            comment: "Missions : Patrouille, Accueil, Garde Hospitaliere inetrvention divers"
        },
        annee2: {
            entreprise: 'Nord Surveillance',
            date: ' 01 Fevrier 2013 - 01 Août 2015',
            title: 'Intervenant sur alarme - CDI ',
            comment: "Missions : Intervention sur les alarmes intrusion, incendie, Rondier et ouverture de site"
        },
        annee3: {
            entreprise: 'SAMSIC',
            title: 'Agent de sécurité',
            comment: "Missions : Mission: Filtrage, controle des entrées et systeme de sécurité incendie"
        },
        annee4: {
            entreprise: 'SDIS 59',
            date: '15 Mars 2008 - à ce jour',
            title: 'Sapeur Pompier Volontaire',
            comment: "Missions : Intervention divers, incendie, Secour à personne"
        },
    }
</script>

<template>
    <div class="experience">
        <div class="experience__title">
            <TitreNiveau2>Mes expériences professionnelles</TitreNiveau2>
        </div>
    
        <div class="annee">
            <div class="job" v-for="annee in parcours">
                <h3 class="job__title">{{ annee.entreprise }}</h3>
                <h4 class="job__info">{{ annee.title }} <span class="separation">|</span> {{ annee.date }}</h4>
                <p class="job__comment">{{ annee.comment }}</p>
            </div>
        </div>
    </div>
</template>

<style scoped>
    .experience {
        background-color: black;
        width: 60%;
        display: flex;
        flex-direction: column;
        align-items: center;
        margin: auto;
    }

    .experience__title {
        text-align: center;
    }

    .material-symbols-outlined {
        font-size: 4em;
    }

    .job__title {
        font-size: 1.25em;
    }

    .job__info {
        font-size: 1.05em;
    }

    .separation {
        font-style: italic;
        color: greenyellow;
    }

    .job__comment {
        text-indent: 2em;
        text-align: justify;
    }

    .annee {
        margin-top: 15px;
        display: flex;
        flex-direction: column;
        gap: 25px;
    }

    .job {
        padding: 15px;
        background-color: black;
        border-radius: 25px;
        box-shadow: -4px 5px 10px greenyellow;
    }

    @media screen and (max-width: 480px) {
        .experience {
            width: 85%;
        }
    }
</style>