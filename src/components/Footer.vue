<script setup>
    import { computed } from 'vue'

const copyright = computed(() =>{
    const currentYear = new Date().getFullYear()
    return `© Copyright ${currentYear} | Mickael Hanon`
});
</script>

<template>
<footer class="footer">
    <div class="footer__content">
        <div class="footer__adress">
            <h3>Mes contacts</h3>
            <address>
                <a href="mailto:hanon.mickael59@gmail.com">hanon.mickael59@gmail.com</a>
                <a href="tel:+0658789000">06-58-78-90-00</a>
                <p>Wasquehal 59290</p>
            </address>
        </div>
        <div class="footer__borderRight"></div>
        <div class="footer__social">
            <h3>Me retrouver</h3>
            <a class="footer__social__icon" href="https://github.com/Diablo5929" target="_blank">
                <img src="@/assets/images/gitHub.png" alt="">
            </a>
            <a class="footer__social__icon" href="https://www.instagram.com/diablo_dev59290?igsh=bjBsMHk4ZGV4MjRu&utm_source=qr" target="_blank">
                <img src="@/assets/images/instagram.png" alt="">
            </a>
        </div>
    </div>
    <div class="footer__copyright">
        <p>Dernières modification le <time datetime="2024-08-18">18 Août 2024</time></p>
        <p class="copyright">{{ copyright }}</p>
    </div>
</footer>
</template>

<style scoped>
.footer__content {
    display: flex;
    justify-content: space-evenly;
    height: 50px;
}

footer {
    border-top: 2px solid greenyellow;
    width: 100%;
}

footer * {
    background-color: black;
    color: greenyellow;
    padding: 10px;
}

.footer__borderRight {
    border-right: 2px solid greenyellow;
}

.footer__adress a{
    text-decoration: none;
}

.footer__adress a:hover {
    opacity: 70%;
    text-decoration: underline;
}

address {
    display: flex;
    flex-direction: column;
}

.footer__copyright {
        text-align: center;
    }

    time {
        font-style: italic;
    }

    .copyright {
        font-style: italic;
        font-size: 0.8em;
    }

    .footer__social__icon:hover {
        opacity: 70%;
    }
</style>