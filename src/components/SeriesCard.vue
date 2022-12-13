<script>
export default {
    props: {
        list: Object
    }
};
</script>

<template>

    <div class="card">
        <img :src="list.thumb" :alt="list.series">
        <h4>
            {{ list.series }}
        </h4>
    </div>

</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

.card {
    width: calc(100% / 6 - 24px);
    margin: 12px;

    h4 {
        color: #fff;
        font-weight: normal;
        text-transform: uppercase;
        font-size: 0.7rem;
        text-align: left;
    }

    img {
        width: 100%;
        height: 150px;
        object-fit: cover;
        object-position: top;
    }
}
</style>