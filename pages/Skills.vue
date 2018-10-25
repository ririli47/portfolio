<template>
    <section class="container">
        <my-header/>
            <div>
                <h1 class="title">
                    Skills
                </h1>
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
        margin-top: 3rem;
        text-align: center;
    }
</style>