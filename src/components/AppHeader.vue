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
                        <div class="border-hover"></div>
                    </a>
                </li>
            </ul>
        </nav>
    </header>
    
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

header {
    background-color: #fff;
    font-size: 0.7rem;
    height: 95px;

    .container {
        display: flex;
        justify-content: space-between;
    }

    ul {
        display: flex;
        justify-content: space-between;
        list-style-type: none;
        height: 95px;

        li {
            position: relative;
            height: 95px;
            padding: 0 10px;

            &:hover .border-hover {
                background-color: $hover;
                height: 4px;
                width: 35px;
                position: absolute;
                bottom: 0;
            }
            
            &:hover a {
                color: $hover;
            }

        }

        li a {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100%;
            text-transform: uppercase;
            color: #5E5F5E;
            font-weight: bold;
        }
    }
}

</style>