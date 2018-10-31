<template>
    <section class="container">
        <my-header/>
            <div>
                <h1 class="topic">
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

<style scoped>
    .container {
        margin-top: 3rem;
        align-items: start;
    }
</style>