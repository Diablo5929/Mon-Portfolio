<template>
    <div class="box">
        <h2>
            <slot></slot>
        </h2>
        <div class="border__bottom"></div>
    </div>
</template>

<style scoped>
    .box {
        display: inline-block;
    }

    h2 {
        font-size: 1.5em;
    }

    .border__bottom {
        border-bottom: 4px solid greenyellow;
        margin : 0px 10%
    }
</style>