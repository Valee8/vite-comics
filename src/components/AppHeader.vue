<script>
export default {
    name: "AppHeader",
    data() {
        return {
            imgLogo: 'dc-logo.png',
            headerLinks: [
                {
                    text: 'Characters',
                    url: '#',
                    active: true,
                },
                {
                    text: 'Comics',
                    url: '#',
                    active: false,
                },
                {
                    text: 'Movies',
                    url: '#',
                    active: false,
                },
                {
                    text: 'Tv',
                    url: '#',
                    active: false,
                },
                {
                    text: 'Games',
                    url: '#',
                    active: false,
                },
                {
                    text: 'Collectibles',
                    url: '#',
                    active: false,
                },
                {
                    text: 'Videos',
                    url: '#',
                    active: false,
                },
                {
                    text: 'Fans',
                    url: '#',
                    active: false,
                },
                {
                    text: 'News',
                    url: '#',
                    active: false,
                },
                {
                    text: 'Shop',
                    url: '#',
                    active: false,
                }

            ]
        };
    },
    methods: {
        getImagePath: function (imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    }
};
</script>

<template>

    <header>
        <nav>
            <div class="container">

                <a href="#">
                    <img :src="getImagePath(`/img/${imgLogo}`)" alt="Logo DC" class="logo">
                </a>

                <ul>
                    <li v-for="(links, index) in headerLinks" :key="index">
                        <a :href="links.url" :class="{ active: links.active }">
                            {{ links.text }}
                            <div :class="{ border: links.active }"></div>
                        </a>
                    </li>
                </ul>
            </div>
        </nav>

        <div class="jumbotron"></div>
    </header>

</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

header {
    font-size: 0.7rem;

    nav {
        background-color: $primary-color;
        height: 95px;

        .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 95px;
        }
    }

    .logo {
        vertical-align: middle;
        height: 70px;
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

            a {
                display: flex;
                justify-content: center;
                align-items: center;
                height: 100%;
                text-transform: uppercase;
                color: #5E5F5E;
                font-weight: bold;

                .border {
                    background-color: $secondary-color;
                    height: 4px;
                    width: 35px;
                    position: absolute;
                    bottom: 0;
                }

                &:hover,
                &.active {
                    color: $secondary-color;
                }
            }

        }
    }

    .jumbotron {
        background-image: url('/img/jumbotron.jpg');
        background-size: cover;
        min-height: 320px;
    }
}
</style>