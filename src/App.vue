<script>
import TheHeader from "./components/TheHeader.vue";
import TheFooter from "./components/TheFooter.vue";
import Cards from "./components/Cards.vue";

export default {
  components: {
    TheHeader,
    TheFooter,
    Cards
  }
}
</script>

<template>
  <TheHeader></TheHeader>

  <main class="main d-flex p-4">
    <div class="card-container p-4">
      

      <Cards></Cards>
    </div>
  </main>

  <TheFooter></TheFooter>
</template>

<style lang="scss">
.main {
  background-color: #D48F38;
}

.card-container {
  background-color: #fff;
}
</style>
