<template>
    <div class="card">
        <div class="poster"><img :src="info.poster" :alt="info.title" /></div>
        <div class="info">
            <h3>{{ info.title }}</h3>
            <div class="author">{{ info.author }}</div>
            <div class="year">{{ info.year }}</div>
            <div class="genre">{{ info.genre }}</div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Card",
    props: ["info"],
};
</script>

<style scoped lang="scss">
@import "@/styles/vars";

.card {
    height: 390px;
    width: 190px;
    margin-right: 40px;
    margin-bottom: 1rem;
    padding: 1rem;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    text-align: center;
    color: $primary-color;
    background-color: rgba($primary-color, 0.1);

    .poster {
        height: 50%;

        img {
            width: 150px;
        }
    }

    h3 {
        margin-bottom: 1rem;
        text-transform: uppercase;
    }

    .author,
    .year {
        margin-bottom: 0.5rem;
        font-size: 18px;
        color: rgba($primary-color, 0.4);
    }
}
</style>
