<script>
export default {
    data() {
        return {
            icons: [
                {
                    text: 'Digital Comics',
                    img: 'buy-comics-digital-comics.png',
                    url: '#',
                },
                {
                    text: 'Dc Merchandise',
                    img: 'buy-comics-merchandise.png',
                    url: '#',
                },
                {
                    text: 'Subscription',
                    img: 'buy-comics-subscriptions.png',
                    url: '#',
                },
                {
                    text: 'Comic Shop Locator',
                    img: 'buy-comics-shop-locator.png',
                    url: '#',
                },
                {
                    text: 'Dc Power Visa',
                    img: 'buy-dc-power-visa.svg',
                    url: '#',
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

    <div class="icons">
        <ul>
            <li v-for="(icon, index) in icons" :key="index">
                <a :href="icon.url">
                    <img :src="getImagePath(`/img/${icon.img}`)" :alt="icon.text" :class="'icons-' + index">
                    {{ icon.text }}
                </a>
            </li>
        </ul>
    </div>

</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

.icons {
    height: 120px;
    background-color: $hover;

    ul {
        display: flex;
        list-style-type: none;
        justify-content: center;
        align-items: center;
        gap: 50px;
        height: 120px;

        li {
            height: 40px;

            &:last-child img {
                transform: scale(0.7);
            }

            img {
                vertical-align: middle;
                padding-right: 5px;
                height: 100%;
            }

            a {
                color: #fff;
                text-transform: uppercase;
                font-size: 0.7rem;
            }
        }
    }
}
</style>