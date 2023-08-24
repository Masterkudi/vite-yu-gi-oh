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

            axios.get(url).then((response) => (
                this.monsters = response.data.results
            ));
        },
    },
    mounted() {
        this.fetchMonsters();
    },
};

</script>

<template>

</template>

<style scoped lang="scss">

</style>