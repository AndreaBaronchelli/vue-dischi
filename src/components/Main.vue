<template>
    <main>
        <div class="content" v-if="!loading">
            <Card v-for="(disc, index) in discs" :key="index" :info="disc" />
        </div>
        <div class="loader" v-else>
            <Load />
        </div>
    </main>
</template>

<script>
import axios from "axios";
import Card from "@/components/Card.vue";
import Load from "@/components/Load.vue";

export default {
    name: "Main",
    components: {
        Card,
        Load,
    },
    data() {
        return {
            discsAPI: "https://flynn.boolean.careers/exercises/api/array/music",
            discs: [],
            loading: true,
        };
    },
    created() {
        this.getDiscs();
    },
    methods: {
        getDiscs() {
            axios
                .get(this.discsAPI)
                .then((res) => {
                    this.discs = res.data.response;
                    this.loading = false;
                })
                .catch((err) => {
                    console.log("Error", err);
                });
        },
    },
};
</script>

<style scoped lang="scss">
.content {
    margin-top: 70px;
    padding-top: 125px;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}

.loader {
    height: 100vh;
}
</style>
