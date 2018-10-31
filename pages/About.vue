<template>
    <section class="container">
        <my-header/>
            <div>
                <h1 class="topic">
                    About
                </h1>
                <my-profile/>
            </div>
        <my-footer/>
    </section>
</template>

<script>
    import MyHeader from '~/components/MyHeader.vue'
    import MyFooter from '~/components/MyFooter.vue'
    import MyProfile from '~/components/MyProfile.vue'

    export default {
        components: {
            MyHeader,
            MyFooter,
            MyProfile
        }
    }
</script>

<style scoped>
    .container {
        margin-top: 3rem;
        align-items: start;
    }
</style>