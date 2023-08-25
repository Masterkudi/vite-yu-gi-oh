<script>
import axios from "axios";

export default {
    data() {
        return {
            monsters: [],
        };
    },
    methods: {
        fetchMonsters() {
            const url = "https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0";

            axios.get(url).then((response) => {
                this.monsters = response.data.data;
        });
        },
    },
    mounted() {
        this.fetchMonsters();
    },
};
</script>

<template>
     <div class="card-bar color-white bg-black">
            Found 20 cards
        </div>
    <div class="row row-cols-5">
       
        <div class="col" v-for="monster in monsters" :key="monster.id">
            <div class="card rounded-0">
                <img :src="monster.image_url" class="card-img-top" alt="...">
                <div class="card-body">
                    <h5 class="card-title">{{ monster.name }}</h5>
                    <p class="card-text">
                        {{ monster.archetype }}
                    </p>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">

.card {
    background-color: #D48F38;
    height: 200px;
}
.card-title {
    color: #fff;
}
.col {
    padding-left: .5rem;
    padding-right: .5rem;
    padding-bottom: .5rem;
}

</style>