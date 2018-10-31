<template>
    <section class="container">
        <my-header/>
            <div>
                <h1 class="topic">
                    Works
                </h1>
                <works-list/>
            </div>
        <my-footer/>
    </section>
</template>

<script>
    import MyHeader from '~/components/MyHeader.vue'
    import MyFooter from '~/components/MyFooter.vue'
    import WorksList from '~/components/MyWorks.vue'

    export default {
        components: {
            MyHeader,
            MyFooter,
            WorksList
        }
    }
</script>

<style scoped>
    .container {
        min-height: 100vh;
        display: flex;
        justify-content: center;
        text-align: center;
        margin-top: 3rem;
        align-items: start;
    }
</style>
