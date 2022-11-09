<script>
export default {
    name: "AppProducts",
    data() {
        return {
            products: [
                {
                    img: "-comics-digital-comics.png",
                    href: "/digitalcomics",
                    name: "DIGITAL COMICS",
                },
                {
                    img: "-comics-merchandise.png",
                    href: "/dcmerchandise",
                    name: "DC MERCHANDISE",
                },
                {
                    img: "-comics-shop-locator.png",
                    href: "/comicshoplocator",
                    name: "COMIC SHOP LOCATOR",
                },
                {
                    img: "-comics-subscriptions.png",
                    href: "/subscription",
                    name: "SUBSCRIPTION",
                },
                {
                    img: "-dc-power-visa.svg",
                    href: "/dcpowervisa",
                    name: "DC POWER VISA",
                },
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
    <main class="products-main">
        <div class="container">
            <nav class="main-nav">
                <ul>
                    <li v-for="(product, index) in products" :key="index">
                        <a href="product.href">
                            <img :src="getPathImg(`../assets/img/buy${product.img}`)" alt="">
                            <p>{{product.name}}</p>
                        </a>
                    </li>
                </ul>
            </nav>
        </div>
    </main>
</template>

<style lang="scss" scoped>
    .products-main {
        background-color: #0282f9;
        height: 150px;

        .container {
            height: 100%;
        }
        .main-nav {
            height: 100%;

            ul {
                height: 100%;
                display: flex;
                justify-content: space-around;
                align-items: center;
                
                li {
                    color: white;

                    a {
                        display: flex;
                        align-items: center;
                        font-size: .8rem;
                        
                        img {
                            width: 50px;
                        }

                        p {
                            margin-left: .5rem;
                        }
                    }
                }
            }
        }
    }
</style>