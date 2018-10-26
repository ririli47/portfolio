<template>
    <section class="container">
        <my-header/>
            <div>
                <h1 class="title">
                    Skills
                </h1>
                <my-skills/>
            </div>
        <my-footer/>
    </section>
</template>

<script>
    import MyHeader from '~/components/MyHeader.vue'
    import MyFooter from '~/components/MyFooter.vue'
    import MySkills from '~/components/MySkills.vue'

    export default {
        components: {
            MyHeader,
            MyFooter,
            MySkills
        }
    }
</script>

<style>
    .container {
        min-height: 100vh;
        justify-content: center;
        margin-top: 3rem;
        text-align: center;
    }
</style>