<template>
    <div class="flex items-center gap-4 text-light-grayish-blue">
        <span class="font-medium tracking-[.4rem]">SHARE</span>
        <button class="btn"><img src="/src/assets/images/icon-facebook.svg" alt=""></button>
        <button class="btn"><img src="/src/assets/images/icon-twitter.svg" alt=""></button>
        <button class="btn"><img src="/src/assets/images/icon-pinterest.svg" alt=""></button>
    </div>
</template>

<style lang="scss" scoped>
    .btn{
        @apply hover:invert;
        @apply w-[1.6rem] aspect-square;
    }
</style>