<template>
    <section class="container">
        <my-header/>
            <div class="profile">
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
    .profile {
        width: 80%;
        margin-left: auto;
        margin-right: auto;
    }
    .container {
        min-height: 100vh;
        display: flex;
        justify-content: center;
        text-align: center;
        margin-top: 3rem;
        align-items: start;
    }

    @media (max-width: 767px) {
        .topic {
            font-size: 2.1rem;
        }
    }

</style>