<script>
export default {
    name: "AppProducts",
    data() {
        return {
            products: [
                {
                    img: "/buy-comics-digital-comics.png",
                    href: "/digitalcomics",
                    name: "DIGITAL COMICS",
                },
                {
                    img: "/buy-comics-merchandise.png",
                    href: "/dcmerchandise",
                    name: "DC MERCHANDISE",
                },
                {
                    img: "/buy-comics-shop-locator.png",
                    href: "/comicshoplocator",
                    name: "COMIC SHOP LOCATOR",
                },
                {
                    img: "/buy-comics-subscriptions.png",
                    href: "/subscription",
                    name: "SUBSCRIPTION",
                },
                {
                    img: "/buy-dc-power-visa.svg",
                    href: "/dcpowervisa",
                    name: "DC POWER VISA",
                },
            ]
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
                            <img :src=" '../assets/img' + product.img" alt="">
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

        ul {
            display: flex;
            justify-content: space-around;
            align-items: center;

            li {
                color: white;
            }
        }
    }
</style>