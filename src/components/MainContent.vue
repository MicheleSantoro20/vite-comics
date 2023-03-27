<script>

    export default {
        name: "MainContent",
    }

</script>

<template>
    <main>
        <div class="main">&rarr; Content goes here &larr;</div>
    </main>

</template>

<style scoped lang="scss">
    @use "../styles/partials/mixin.scss";

    main {
        width: 100%;
        height: 200px;
        background-color: #1c1c1c;
    }
    .main {
        @include mixin.page-margin;
        color: white;
        line-height: 200px;
        font-size: 40px;
    }

</style>