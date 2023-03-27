<script>

    export default {
        name: "MainNavBar",
        data () {
            return {
                MainNav: [
                    {
                        name: "DIGITAL COMICS",
                        img: "../src/assets/buy-comics-digital-comics.png",
                    },
                    {
                        name: "DC MERCHANDISE",
                        img: "../src/assets/buy-comics-merchandise.png",
                    },
                    {
                        name: "SUBSCRIPTION",
                        img: "../src/assets/buy-comics-subscriptions.png",
                    },
                    {
                        name: "COMIC SHOP LOCATOR",
                        img: "../src/assets/buy-comics-shop-locator.png",
                    },
                    {
                        name: "DC POWER VISA",
                        img: "../src/assets/buy-comics-power-visa.png",
                    },
                ]
            }
        }
    }

</script>

<template>
    <div class="MainNavBar">
        <ul>
            <li class="mainNav" v-for="element in MainNav">{{ element.img }} {{ element.name }}</li>
        </ul>
    </div>


</template>

<style scoped lang="scss">
    @use "../styles/partials/mixin.scss";

    .MainNavBar {
        width: 100%;
        height: 200px;
        background-color: #0282f9;
    }
    .mainNav {
        @include mixin.page-margin;
        color: white;
        line-height: 200px;
        font-size: 20px;
    }

</style>