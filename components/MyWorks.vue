<template>
    <section class="works-list">
        <div v-for="work in works" v-bind:key="work.id" class="work">
            <div class="card">
                <div class="card-image waves-effect waves-block waves-light">
                    <img class="activator" :src="work.logo">
                </div>
                <div class="card-content">
                    <span class="card-title activator grey-text text-darken-4">{{ work.name }}</span>
                    <p><a :href="work.link" target="_blink" >{{ work.name }}</a></p>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        name: 'WorksList',
        data() {
            return {
                works: [
                    {id: 1, name: 'Tasker', link: 'https://ririli-tasker.herokuapp.com/', logo: require("~/assets/img/tasker_logo.png")},
                    {id: 2, name: 'IdeaCafe', link: 'https://ideacafe.herokuapp.com/', logo: require("~/assets/img/ideacafe_logo.png")},
                    {id: 3, name: 'Portfolio', link: 'https://www.ririli.net/', logo: require("~/assets/img/ideacafe_logo.png")},
                ]
            }
        }
    }
</script>

<style>
    .works-list {
        display: flex;
        flex-wrap: wrap;
        margin-bottom: 100px;
    }
    .work {
        max-width: 33.3%;
        flex: 33.3%;
    }
    .card {
        width: 80%;
        margin-left: auto;
        margin-right: auto;
    }
    .card-image {
        width: 60%;
        margin-left: auto;
        margin-right: auto;
        padding-top: 10%;
    }
</style>