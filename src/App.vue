<template>
  <div class="min-w-[320px] min-h-screen p-6 flex flex-col gap-6 bg-light-grayish-blue">
    <main class="grow flex justify-center items-center">
      <Card />
    </main>
    <footer>
      <Attribution myName="Jasper Lai" />
    </footer>
  </div>
</template>
<script>
import Attribution from './components/Attribution.vue'
import Card from './components/Card.vue'
export default{
  components:{
    Attribution, Card
  }
}
</script>