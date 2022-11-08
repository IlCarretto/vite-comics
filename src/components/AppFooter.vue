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
            ]
        }
    }
}
</script>

<template>
    <footer>
        <div class="container">
            <div class="footer-top">
                <div class="footer-list">
                    <div class="first-list">
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
                    <div class="second-list">
                        <ul>
                            <li v-for="dc in dcList">
                                <a :class="{'list-title' : dc.title}" href="">{{dc.name}}</a>
                            </li>
                        </ul>
                    </div>
                    <div class="third-list">
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

            </div>
    </footer>
</template>

<style lang="scss" scoped>
    footer {
        width: 100%;
        height: 350px;
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
                align-items: center;

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
            width: 400px;
            overflow: hidden;
            }
        }   
        .footer-bottom {
            width: 100%;
            height: 170px;
            background-color: #303030;
        }
    }
</style>