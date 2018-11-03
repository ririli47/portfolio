<template>
    <section class="container">
        <my-header/>
            <div class="home">
                <h1 class="title">
                    ririli's Portfolio
                </h1>
                <router-view/>
            </div>
        <my-footer/>
    </section>
</template>

<script>
    import MyHeader from '~/components/MyHeader.vue'
    import MyFooter from '~/components/MyFooter.vue'

    export default {
        components: {
            MyHeader,
            MyFooter
        }
    }
</script>

<style>
    .container {
        min-height: 100vh;
        display: flex;
        justify-content: center;
        text-align: center;
        align-items: center;
    }
    .title {
        font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
        display: block;
        font-weight: 300;
        font-size: 80px;
        color: #35495e;
        letter-spacing: 1px;
    }

    .subtitle {
        font-weight: 300;
        font-size: 42px;
        color: #526488;
        word-spacing: 5px;
        padding-bottom: 15px;
    }

    .links {
        padding-top: 15px;
    }

    @media (max-width: 767px) {
        .title {
            font-size: 40px;
        }
    }

</style>

