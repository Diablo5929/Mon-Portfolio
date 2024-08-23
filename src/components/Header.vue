<script setup>
import { ref } from 'vue'

let showMenu = ref( false )
</script>

<template>
    <header>
        <nav>
            <router-Link class="link__img" to="/">
                <img src="@/assets/images/MikeDev.png" alt="Mickael Logo">
            </router-Link>

            <div class="sideNav__background" v-if="showMenu" @click="showMenu=false"></div>

            <div class="sideNav" v-if="showMenu">
                <span class="material-symbols-outlined link" @click="showMenu=false">close</span>
                <ul class="sideNav__list">
                    <router-Link to="/#about" @click="showMenu=false">Présentation</router-Link>
                    <router-Link to="/#projets" @click="showMenu=false">Projets</router-Link>
                    <router-Link to="/#contact" @click="showMenu=false">Contact</router-Link>
                </ul>
            </div>

            <span class="material-symbols-outlined burger-icon link" @click="showMenu=true">Menu</span>


            <div class="nav__link">
                <router-link id="about__link" to="/#about">Présentation</router-link>
                <span>|</span>
                <router-link id="project__link" to="/#projets">Projets</router-link>
                <span>|</span>
                <router-link id="contact__link" to="/#contact">Contact</router-link>
            </div>
        </nav>
    </header>
</template>


<style scoped>
    header {
        position: fixed;
        background-color: rgb(0, 0, 0);
        width: 100%;
        height: 50px;
        top: 0;
        padding: 15px;
        border-bottom: 5px solid yellowgreen;
        color: greenyellow;
        right: 0px;
    }

    nav {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .link__img {
        padding: 5px;
    }

    img {
        width: 50px;
        padding-left: 30;
        height: 50px;
    }

    .nav__link * {
        font-size: 1.5em;
        padding: 5.5px;
        text-decoration: none;
        color: greenyellow;
    }

    .nav__link a {
        padding: 15px;
    }

    a:hover {
        opacity: 70%;
        text-decoration: underline;
    }

    .burger-icon {
        display: none;
    }

    .sideNav {
        width: 65%;
        height: 100%;
        box-sizing: border-box;
        position: fixed;
        top: 85px;
        right: 0;
        background-color: black;
        padding: 10px;
        border: 3px solid greenyellow;
        border-top: none;
        border-right: none;
    }

    .sideNav__background {
        position: fixed;
        top: 0;
        left: 0;
        height: 100%;
        width: 100%;
    }
    
    .sideNav__list {
        display: flex;
        flex-direction: column;
        gap: 15px;
        font-size: 1.1em;
        padding-right: 1em;
    }

    .sideNav a {
        color: greenyellow;
        text-decoration: none;
    }

    .sideNav a:hover {
        text-decoration: underline;
    }


    .link {
        cursor: pointer;
    }

    @media screen and (max-width: 480px) {
        .burger-icon {
            display: block;
            color: greenyellow;
            margin-right: 10%;
        }

        .nav__link {
            display: none;
        }
    }
        
</style>