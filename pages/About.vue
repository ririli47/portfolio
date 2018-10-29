<template>
    <section class="container">
        <my-header/>
            <div>
                <h1 class="title">
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


<style>
    .container {
        min-height: 100vh;
        display: flex;
        justify-content: center;
        margin-top: 3rem;
        text-align: center;
    }
</style>