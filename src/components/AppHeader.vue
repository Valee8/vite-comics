<script>
export default {
    data() {
        return {
            imgLogo: 'dc-logo.png',
        };
    },
    methods: {
        getImagePath: function(imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    }
};
</script>

<template>

    <header>
        <a href="#">
            <img :src="getImagePath(`/img/${imgLogo}`)" alt="Logo DC">
        </a>
    </header>
    
</template>

<style lang="scss" scoped>

header {
    background-color: #fff;
}

</style>