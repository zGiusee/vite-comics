<script>
export default {
    data() {
        return {
            footerList: [
                {
                    listTitle: 'DC COMICS',
                    liLinks: [
                        {
                            linkName: 'Characters',
                            url: '#'
                        },
                        {
                            linkName: 'Comics',
                            url: '#'
                        },
                        {
                            linkName: 'Movies',
                            url: '#'
                        },
                        {
                            linkName: 'Tv',
                            url: '#'
                        },
                        {
                            linkName: 'Gameplay',
                            url: '#'
                        },
                        {
                            linkName: 'Videos',
                            url: '#'
                        },
                        {
                            linkName: 'News',
                            url: '#'
                        },
                    ]
                },
                {
                    listTitle: 'DC',
                    liLinks: [
                        {
                            linkName: 'Terms Of Use',
                            url: '#'
                        },
                        {
                            linkName: 'Privacy policy (new)',
                            url: '#'
                        },
                        {
                            linkName: 'Ad Choices',
                            url: '#'
                        },
                        {
                            linkName: 'Advertising',
                            url: '#'
                        },
                        {
                            linkName: 'Jobs',
                            url: '#'
                        },
                        {
                            linkName: 'Subscription',
                            url: '#'
                        },
                        {
                            linkName: 'Talent Workshop',
                            url: '#'
                        },
                        {
                            linkName: 'CPSC Certificates',
                            url: '#'
                        },
                        {
                            linkName: 'Ratings',
                            url: '#'
                        },
                        {
                            linkName: 'Shop Help',
                            url: '#'
                        },
                        {
                            linkName: 'Contact Us',
                            url: '#'
                        },
                    ]
                },
                {
                    listTitle: 'SITES',
                    liLinks: [
                        {
                            linkName: 'DC',
                            url: '#'
                        },
                        {
                            linkName: 'MAD Magazine',
                            url: '#'
                        },
                        {
                            linkName: 'DC Kids',
                            url: '#'
                        },
                        {
                            linkName: 'DC Universe',
                            url: '#'
                        },
                        {
                            linkName: 'DC Power Visa',
                            url: '#'
                        },
                    ]
                },
                {
                    listTitle: 'SHOP',
                    liLinks: [
                        {
                            linkName: 'Shop DC',
                            url: '#'
                        },
                        {
                            linkName: 'Shop DC Collectibles',
                            url: '#'
                        },
                    ]
                },
            ],
            Socials: [
                {
                    socialLogo: '../img/footer-facebook.png',
                    url: '#',
                },
                {
                    socialLogo: '../img/footer-periscope.png',
                    url: '#',
                },
                {
                    socialLogo: '../img/footer-pinterest.png',
                    url: '#',
                },
                {
                    socialLogo: '../img/footer-twitter.png',
                    url: '#',
                },
                {
                    socialLogo: '../img/footer-youtube.png',
                    url: '#',
                },
            ]
        }
    },
    methods: {
        getImagePath: function (imgPath) {
            let url = new URL(imgPath, import.meta.url).href;
            return url
        }
    },
}
</script>

<template>
    <footer>
        <div class="footer-bg top-footer py-5">
            <div class="container">

                <div class="row">

                    <!-- LEFT FOOTER SIDE -->
                    <div class="col-6">
                        <div class="footer_list_container">
                            <ul v-for="(list, index) in footerList" :key="index">
                                <h3>
                                    {{ list.listTitle }}
                                </h3>
                                <li v-for="(link, index) in list.liLinks" :key="index">
                                    <a :href="link.url">{{ link.linkName }}</a>
                                </li>
                            </ul>
                        </div>
                    </div>

                    <!-- RIGHT FOOTER SIDE -->
                    <div class="col-6">
                        <div class="d-flex justify-content-end ">
                            <img class="logo" src=" ../img/dc-logo-bg.png" alt="">
                        </div>
                    </div>

                </div>
            </div>
        </div>

        <div class="bottom-footer">
            <div class="container">
                <div class="row">
                    <!-- CREDITS SECTION -->
                    <div class="col-6">
                        <div class="d-flex align-items-center h-100">
                            <a class="sign-up-button" href="">SIGN-UP-NOW!</a>
                        </div>
                    </div>

                    <div class="col-6">
                        <div class="d-flex justify-content-end align-items-center">
                            <span>FOLLOW US</span>
                            <ul>
                                <li v-for="(social, index) in Socials">
                                    <a :href="social.url"><img :src="getImagePath(social.socialLogo)" alt=""></a>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use '../styles/general.scss' as *;
@use '../styles/partials/variables' as *;

footer {
    position: relative;

    .footer-bg {
        background-image: url(../img/footer-bg.jpg);
        background-repeat: no-repeat;
        background-size: cover;
    }

    .logo {
        position: absolute;
        top: -45px;
        width: 650px;
    }

    .footer_list_container {
        display: flex;
        flex-wrap: wrap;

        h3 {
            font-weight: bold;
        }

        ul {
            list-style-type: none;
            padding: 0px 20px;
            margin: 0px 15px;
            color: white;

            li {

                a {
                    text-decoration: none;
                    color: white;

                    &:hover {
                        text-decoration: underline;
                    }
                }
            }
        }
    }

    .bottom-footer {
        padding: 35px 0px;
        position: relative;
        z-index: 999;
        background-color: $dc_grey;
        display: flex;
        align-items: center;

        span {
            color: $dc_blue;
            font-weight: bold;
            font-size: 20px;
        }

        ul {
            list-style-type: none;
            display: flex;
            margin-bottom: 0px;
        }

        ul li {
            padding: 10px;
            cursor: pointer;
        }
    }

    .sign-up-button {
        color: white;
        font-weight: bold;
        font-size: 20px;
        text-decoration: none;
        padding: 7px 12px;
        border: 3px solid $dc_blue;
    }

}
</style>