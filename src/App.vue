<script>
import TheHeader from "./components/TheHeader.vue";
import TheFooter from "./components/TheFooter.vue";
import MosterCards from "./components/MonsterCards.vue";

export default {
  components: {
    TheHeader,
    TheFooter
  }
}
</script>

<template>

  <TheHeader></TheHeader>

  <main>
    <div class="card-container">
      Lorem ipsum, dolor sit amet consectetur adipisicing elit. Deserunt molestiae, velit itaque aliquid quisquam quidem quos nostrum mollitia blanditiis asperiores atque corrupti, voluptatum voluptatem, laudantium ea amet libero similique architecto.

      <MonsterCards></MonsterCards>
    </div>
  </main>

  <TheFooter></TheFooter>

</template>

<style lang="scss">
  main {
    background-color: #D48F38;
  }
  .card-container {
    background-color: #fff;
  }
</style>
