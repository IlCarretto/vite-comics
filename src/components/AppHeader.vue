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
        <header>
            <div class="logo">
                <img src="../assets/img/dc-logo.png" alt="">
            </div>
        </header>
    </div>
</template>

<style scoped>
    .band {
        width: 100%;
        height: 25px;
        background-color: black;
    }

    header {
        .logo {
            width: 80px;
        }
    }
</style>