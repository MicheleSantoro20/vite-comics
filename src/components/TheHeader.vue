<script>
export default {
    name: "TheHeader",
    data() {
    return {
        navbar: ["CHARACTERS", "COMICS", "MOVIES", "TV", "GAMES", "COLLECTIBLES", "VIDEOS", "FANS", "NEWS", "SHOP"]
        };
    },
}

</script>



<template>
    <header class="header">
        <div><img src="../assets/dc-logo.png" alt=""></div>
        <ul>
            <li class="header-navbar" v-for="(element) in navbar" href="#"> {{ element }}</li>
        </ul>
    </header>

</template>



<style scoped lang="scss">

    @use "../styles/partials/mixin.scss";
    .header-navbar {
        list-style: none;
        display: inline-block;
        padding: 20px 0px;
        margin-left: 30px;
        color: gray;
        font-weight: bold;
        font-size: 15px;

        &:hover {
            color: #0282f9;
            border-bottom: 3px solid #0282f9;
            cursor: crosshair;
        }
    }
    .header {
        @include mixin.d-flex-between;
        @include mixin.page-margin;
        padding: 15px 0px;
        
    }
</style>