<template>
    <header>
        <img src="../assets/images/logo.png" alt="Spotify Logo" />
    </header>
</template>

<script>
export default {
    name: "Header",
};
</script>

<style scoped lang="scss">
@import "../styles/vars";

header {
    width: 100%;
    position: fixed;
    top: 0;
    left: 0;
    background-color: rgba($primary-color, 0.05);

    img {
        width: 50px;
        margin: 0.5rem;
    }
}
</style>
