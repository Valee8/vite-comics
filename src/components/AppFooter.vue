<script>

export default {
    data() {
        return {

        }
    }
}

</script>

<template>
    <footer>

    </footer>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

footer {
    background-image: url('/img/dc-logo-bg.png'), url('/img/footer-bg.jpg');
    background-repeat: no-repeat, repeat-x;
    background-position: 75%, center;
    background-size: 30%, cover;
    min-height: 300px;
}
</style>