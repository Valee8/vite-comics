<script>

export default {
    data() {
        return {
            textButton: 'Sign-Up Now!',
            textFollow: 'Follow Us',
            imgSocials: [
                {
                    text: 'Facebook',
                    img: 'footer-facebook.png'
                },
                {
                    text: 'Twitter',
                    img: 'footer-twitter.png'
                },
                {
                    text: 'Youtube',
                    img: 'footer-youtube.png'
                },
                {
                    text: 'Pinterest',
                    img: 'footer-pinterest.png'
                },
                {
                    text: 'Periscope',
                    img: 'footer-periscope.png'
                },
            ],
            footerLinks: [
                {
                    title: 'DC Comics',
                    links: [
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
                            text: 'TV',
                            url: '#',
                        },
                        {
                            text: 'Games',
                            url: '#',
                        },
                        {
                            text: 'Videos',
                            url: '#',
                        },
                        {
                            text: 'News',
                            url: '#',
                        }
                    ]
                
                },

                {
                    title: 'DC',
                    links: [
                        {
                            text: 'Term Of Use',
                            url: '#',
                        },
                        {
                            text: 'Privacy Policy (New)',
                            url: '#',
                        },
                        {
                            text: 'Ad Choices',
                            url: '#',
                        },
                        {
                            text: 'Advertising',
                            url: '#',
                        },
                        {
                            text: 'Jobs',
                            url: '#',
                        },
                        {
                            text: 'Subscriptions',
                            url: '#',
                        },
                        {
                            text: 'Talent Workshops',
                            url: '#',
                        },
                        {
                            text: 'CPSC Certificates',
                            url: '#',
                        },
                        {
                            text: 'Ratings',
                            url: '#',
                        },
                        {
                            text: 'Shop Help',
                            url: '#',
                        },
                        {
                            text: 'Contact Us',
                            url: '#',
                        }
                    ]
                
                },

                {
                    title: 'Sites',
                    links: [
                    {
                            text: 'DC',
                            url: '#',
                        },
                        {
                            text: 'MAD Magazine',
                            url: '#',
                        },
                        {
                            text: 'DC Kids',
                            url: '#',
                        },
                        {
                            text: 'DC Universe',
                            url: '#',
                        },
                        {
                            text: 'DC Power Visa',
                            url: '#',
                        }
                    ]
                
                },
                {
                    title: 'Shop',
                    links: [
                        {
                            text: 'Shop DC',
                            url: '#',
                        },
                        {
                            text: 'Shop DC Collectibles',
                            url: '#',
                        },
                    ]
                
                },

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
    <footer>

        <div class="container">
            <div class="list-links">
                <div v-for="(footer, index) in footerLinks" :key="index" class="footer-list">
                    <h3>
                        {{footer.title}}
                    </h3>

                    <ul>
                        <li v-for="link in footer.links" :key="index">
                            <a :href="link.url">
                                {{link.text}}
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>

        <div class="socials">

            <div class="container">

                <a href="#" class="link-button">
                    {{textButton}}
                </a>

                <div class="social-links">
                    <h3>
                    {{textFollow}}
                    </h3>

                    <ul>
                        <li v-for="(images, index) in imgSocials" :key="index">
                            <a href="#">
                                <img :src="getImagePath(`/img/${images.img}`)" :alt="images.text">
                            </a>
                        </li>
                    </ul>
                </div>

            </div>

        </div>

    </footer>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

footer {
    background-image: url('/img/dc-logo-bg.png'), url('/img/footer-bg.jpg');
    background-repeat: no-repeat, no-repeat;
    background-position: 75%, left top;
    background-size: 30%, cover;
    color: #fff;

    .list-links {
        display: flex;
        max-width: 35%;
        position: relative;
        padding: 40px 0 60px 0;
    }

    h3 {
        text-transform: uppercase;
        font-size: 1rem;
    }

    .footer-list {
        width: calc(100% / 3);

        &:last-child {
            position: absolute;
            bottom: 45px;
            left: 0;
        }

        ul {
            list-style-type: none;
            padding-top: 10px;

            li {
                line-height: 15px;

                a {
                color: rgba(255, 255, 255, .6);
                font-size: 0.6rem;
                }

            }

        }
    }

    .socials {
        height: 90px;
        background-color: #303030;

        .social-links {
            display: flex;
        }

        .container {  
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 90px;
        }

        h3 {
            align-self: center;
            padding-right: 30px;
            color: $hover;
        }

        .link-button {
            border: 2px solid $hover;
            color: #fff;
            text-transform: uppercase;
            padding: 8px;
            font-size: 0.8rem;
            font-weight: bold;
        }
        
        ul {
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 20px;
            list-style-type: none;
            
            img {
                width: 30px;
            }
        }
    }
}
</style>