<script>
export default {
    data() {
        return {
            imgLogo: 'dc-logo.png',
            headerLinks: [
                {
                    text: 'Characters',
                    url: '#',
                },
                {
                    text: 'Comics',
                    url: '#',
                },
                {
                    text: 'Movies',
                    url: '#',
                },
                {
                    text: 'Tv',
                    url: '#',
                },
                {
                    text: 'Games',
                    url: '#',
                },
                {
                    text: 'Collectibles',
                    url: '#',
                },
                {
                    text: 'Videos',
                    url: '#',
                },
                {
                    text: 'Fans',
                    url: '#',
                },
                {
                    text: 'News',
                    url: '#',
                },
                {
                    text: 'Shop',
                    url: '#',
                }

            ]
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

        <nav>
            <ul>
                <li v-for="links in headerLinks">
                    <a :href="links.url">
                        {{links.text}}
                    </a>
                </li>
            </ul>
        </nav>
    </header>
    
</template>

<style lang="scss" scoped>

header {
    background-color: #fff;
}

</style>