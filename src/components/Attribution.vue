<template>
    <div class="attribution">
        Challenge by <a href="https://www.frontendmentor.io?ref=challenge" target="_blank">Frontend Mentor</a>.
        Coded by <a :href="gitLink">{{ myName }}</a>.
    </div>
</template>
<script>
    export default{
        props:{
            gitLink:{
                type:String,
                default:'#'
            },
            myName:{
                type:String,
                default:'I don\'t have name!'
            }
        }
    }
</script>
<style lang="scss" scoped>
.attribution { font-size: 11px; text-align: center; }
.attribution a { color: hsl(228, 45%, 44%); }
</style>