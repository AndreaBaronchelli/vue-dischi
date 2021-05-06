<template>
    <div class="loader">
        <img src="../assets/images/vinyl_PNG5.png" alt="" />
        <div class="text">Loading...</div>
    </div>
</template>

<script>
export default {
    name: "Load",
};
</script>

<style scoped lang="scss">
@import "@/styles/vars";

.loader {
    height: 100%;
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background-color: rgba($primary-color, 0.05);

    img {
        width: 200px;
        margin-bottom: 2rem;
        animation: rotate 1s infinite linear forwards;
    }

    .text {
        font-size: 24px;
        text-transform: uppercase;
        color: $primary-color;
    }
}

@keyframes rotate {
    from {
        transform: rotate(0deg);
    }

    to {
        transform: rotate(360deg);
    }
}
</style>
