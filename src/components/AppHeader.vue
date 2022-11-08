<script>
export default {
    name: "AppHeader",
    data() {
        return {
           items: [
                {
                    name: "Characters",
                    href: "/characters",
                    active: true
                },
                {
                    name: "Comics",
                    href: "/comics",
                    active: false
                },
                {
                    name: "Movies",
                    href: "/movies",
                    active: false
                },
                {
                    name: "TV",
                    href: "/tv",
                    active: false
                },
                {
                    name: "Games",
                    href: "/games",
                    active: false
                },
                {
                    name: "Collectibles",
                    href: "/collectibles",
                    active: false
                },
                {
                    name: "Videos",
                    href: "/videos",
                    active: false
                },
                {
                    name: "Fans",
                    href: "/fans",
                    active: false
                },
                {
                    name: "News",
                    href: "/news",
                    active: false
                },
                {
                    name: "Shop",
                    href: "/shop",
                    active: false
                },
           ]
        }
    }
}
</script>

<template>
    <div class="band"></div>
    <div class="container">
        <header class="header">
            <div class="logo">
                <img src="../assets/img/dc-logo.png" alt="">
            </div>
            <nav class="header-nav">
                <ul>
                    <li v-for="(item, index) in items" :key="index">
                        <a :class="{'active' : item.active}" :href="item.href">{{item.name}}</a>
                    </li>
                </ul>
            </nav>
        </header>
    </div>
</template>

<style lang="scss" scoped>
    .band {
        width: 100%;
        height: 25px;
        background-color: black;
    }

    .header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 1rem 0;
        .logo {
            width: 80px;
        }

        &-nav {
            ul {
                display: flex;

                text-transform: uppercase;

                li {
                    padding: 0 .5rem;
                    font-size: .8rem;
                    font-weight: 700;
                    color: #5a648a;
                    
                    a.active {
                        color: #0282f9;
                    }
                }
            }
        }
    }
</style>