<script setup>
    import { ref } from 'vue'

    import TitreNiveau2 from './TitreNiveau2.vue';
    import Courses from '@/components/Courses.vue';
    import Experiences from '@/components/Experiences.vue';
    import Skills from '@/components/Skills.vue';

    
  const presentationFilter = ref( 'courses' )
</script>

<template>
    <Header/>
        <div id="about">
        <div class="presentation">
            <div class="presentation__text">
                <TitreNiveau2>Présentation</TitreNiveau2>
                <p>Je suis Mickael Hanon, passionné par le développement web. Je suis un développeur web débutant avec une forte motivation et un grand intérêt pour le front et le back end. <br>
                    Malgré mon expérience récente, j'ai acquis de solides compétences en HTML, CSS, JavaScript et j'ai déjà réalisé plusieurs projets personnels qui me permettent de mettre en avant mes capacités. <br>
                    Dans ce portfolio, vous découvrirez quelques exemples de mes réalisations, qui illustrent ma passion pour le développement web et mon aptitude à apprendre rapidement. <br>
                    Je suis impatient de discuter de vos besoins et de découvrir comment je peux vous aider à concrétiser vos projets web. N'hésitez pas à me contacter pour toute question ou pour en savoir plus sur mes réalisations.</p>
                <router-link class="CTA" :to="{hash:'#contact'}">Me contacter</router-link>
            </div>
        
            <img src="@/assets/images/mickael.jpg" alt="Photo de Mickael">
        </div>
    
        <div class="about__filter">
            <button class="about__filter__button CTA" @click="presentationFilter='courses'">Parcours</button>
            <button class="about__filter__button CTA" @click="presentationFilter='experiences'">Expériences</button>
            <button class="about__filter__button CTA" @click="presentationFilter='skills'">Compétences</button>  
        </div>
    
        <div class="about__content">
            <Courses v-if="presentationFilter === 'courses' "/>
        
            <Experiences v-if="presentationFilter === 'experiences' "/>
        
            <Skills v-if="presentationFilter === 'skills' "/>
        </div>
    </div>
</template>

<style scoped>
    .presentation {
        background-color: black;
        width: 60%;
        display: flex;
        align-items: center;
        margin: auto;
    }


    .presentation__text {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: 15px;
    }

    .presentation__text p {
        width: 60%;
        text-align: justify;
        text-indent: 5%;
    }

    img {
       width: 150px;
        height: 25%;
        border-radius: 50%;
        box-shadow: -4px 5px 25px greenyellow;
        margin-top: 5x;
    }


    .about__filter {
        display: flex;
        gap: 15px;
        margin: 15px 0;
        justify-content: center;
        background-color: black;
        border-bottom: 3px solid greenyellow;
    }
    .about__content {
        margin-bottom: 15px;
        margin-bottom: 2em;
    }


    @media screen and (max-width: 480px) {
        .presentation {
            flex-direction: column-reverse;
            padding: 10px 0;
        }
        .presentation__text p {
            width: 50%;
        }
        img {
            width: 85%;
        }
    }
</style>