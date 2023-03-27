<script>

    export default {
        name: "FooterSection",
        data() {
            return {
                FooterNav : [
                    {
                        Name: "DC COMICS",
                        NavElement: ["Characters", "Comics", "Movies", "TV", "Games", "Videos", "News"]
                    },
                    {
                        Name: "DC",
                        NavElement: ["Terms of Use", "Privacy Policy (New)", "Ad Choiches", "Advertising", "jobs", "Subscriptions", "Talent Workshops", "CPSC", "Ratings", "Shop Help", "Contact Is"]
                    },
                    {
                        Name: "sites",
                        NavElement: ["DC", "MAD Magazine", "DC Kid", "DC Universe", "DC Power Visa"]
                    },
                    {
                        Name: "Shop",
                        NavElement: ["Shop DC", "Shop DC Collectibles"]
                    },
                ]
            }
        }
    }

</script>

<template>
    <footer>
        <div class="wrapper">
            <div class="FooterList">
                <ul v-for="element in FooterNav"> 

                    <li class="ListName">
                        {{element.Name}}
                        <ul>
                            <li class="ListItem" v-for="contenuti in element.NavElement">{{ contenuti }}</li>
                        </ul>
                    </li>
                </ul>
            </div>
            <div>
                <img src="../assets/dc-logo-bg.png" alt="">
            </div>
        </div>
    </footer>

</template>

<style scoped lang="scss">
    @use "../styles/partials/mixin.scss";

    .wrapper {
        @include mixin.page-margin;
        display: flex;
    }

    footer {
        height: 400px;
        background-image: url(../assets/footer-bg.jpg);
    }
    li {
        color: white;
        list-style: none;
    }
    .FooterList {
        display: flex;
        width: 50%;
        flex-wrap: wrap;
    }

    ul {
        width: calc(100% /3);
        height: 0px;
    }

    .ListName {
        width: 100%;
        padding: 5px;
        font-size: 30px;
        font-weight: bold;
    }

    .ListItem {
        font-size: 15px;
        font-weight: normal;
        color: lightgray;
    }
</style>