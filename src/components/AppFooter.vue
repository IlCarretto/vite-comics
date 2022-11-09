<script>
export default {
    name: "AppFooter",
    data() {
        return {
            comicsList: [
                {
                    name: "DC COMICS",
                    title: true
                },
                {
                    name: "Characters"
                },
                {
                    name: "Comics"
                },
                {
                    name: "Movies"
                },
                {
                    name: "TV"
                },
                {
                    name: "Games"
                },
                {
                    name: "Videos"
                },
                {
                    name: "News"
                },
            ],
            shop: [
                {
                    name: "SHOP",
                    title: true
                },
                {
                    name: "Shop DC"
                },
                {
                    name: "SHOP DC Collectibles"
                }
            ],
            dcList: [
                {
                    name: "DC",
                    title: true
                },
                {
                    name: "Terms of Use"
                },
                {
                    name: "Privacy policy (new)"
                },
                {
                    name: "Ad Choices"
                },
                {
                    name: "Advertising"
                },
                {
                    name: "Jobs"
                },
                {
                    name: "Subscriptions"
                },
                {
                    name: "Talent Workshops"
                },
                {
                    name: "CPSC Certificates"
                },
                {
                    name: "Ratings"
                },
                {
                    name: "Shop Help"
                },
                {
                    name: "Contact Us"
                }
            ],
            sitesList: [
                {
                    name: "SITES",
                    title: true
                },
                {
                    name: "DC"
                },
                {
                    name: "MAD Magazine"
                }
            ],
            socialsIcons: [
                {
                    name: "-facebook.png"
                },
                {
                    name: "-periscope.png"
                },
                {
                    name: "-pinterest.png"
                },
                {
                    name: "-twitter.png"
                },
                {
                    name: "-youtube.png"
                }
            ]
        }
    },
    methods: {
        getPathImg(url) {
            return new URL(url, import.meta.url).href;
        }
    }
}
</script>

<template>
    <footer>
        <div class="container">
            <div class="footer-top">
                <div class="footer-list">
                    <div class="col">
                        <ul>
                            <li v-for="comic in comicsList">
                                <a :class="{'list-title' : comic.title}" href="">{{comic.name}}</a>
                            </li>
                        </ul>
                        <ul>
                            <li v-for="shopItem in shop">
                                <a :class="{'list-title' : shopItem.title}" href="">{{shopItem.name}}</a>
                            </li>
                        </ul>
                    </div>
                    <div class="col">
                        <ul>
                            <li v-for="dc in dcList">
                                <a :class="{'list-title' : dc.title}" href="">{{dc.name}}</a>
                            </li>
                        </ul>
                    </div>
                    <div class="col">
                        <ul>
                            <li v-for="site in sitesList">
                                <a :class="{'list-title' : site.title}" href="">{{site.name}}</a>
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="footer-logo">
                    <img src="../assets/img/dc-logo-bg.png" alt="">
                </div>
            </div>
        </div>
            <div class="footer-bottom">
                <div class="container">
                    <div class="btn-container">
                        <a class="btn">SIGN-UP NOW!</a>
                    </div>
                    <div class="socials">
                        <h3 class="socials-title">FOLLOW US</h3>
                        <div v-for="socialsIcon in socialsIcons" class="circle-icon">
                            <a href="">
                                <img :src="getPathImg(`../assets/img/footer${socialsIcon.name}`)" alt="">
                            </a>
                        </div>
                    </div>
                </div>
            </div>
    </footer>
</template>

<style lang="scss" scoped>
    footer {
        width: 100%;
        height: 400px;
        background-image: url(../assets/img/footer-bg.jpg);

        .container {
            height: 100%;
        }
        .footer-top {
            width: 100%;
            height: 100%;
            display: flex;
            justify-content: space-between;

            .footer-list {
                display: flex;
                margin-top: 3rem;

                ul {
                    padding-right: .5rem;

                    li:not(:first-child) {
                        font-size: .8rem;
                        color: grey;
                        padding: .3rem 0;
                    }

                    .list-title {
                        color: white;
                        font-weight: 600;
                        padding-bottom: .5rem;
                    }
                }

            }
            .footer-logo {
            width: 450px;
            overflow: hidden;
            }
        }   
        .footer-bottom {
            width: 100%;
            height: 76px;
            background-color: #303030;

            .container {
                display: flex;
                justify-content: space-between;
                align-items: center;

                .btn {
                    border: 1px solid #0282f9;
                    color: white;
                    padding: .8rem;
                }

                .socials {
                    display: flex;

                    &-title {
                        color: #0282f9;
                        display: flex;
                        align-items: center;
                    }

                    .circle-icon {
                        margin-left: 1rem;
                    }
                }
            }
        }
    }
</style>