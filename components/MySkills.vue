<template>
    <section class="skill-list">
        <h2>Languages</h2>
        <div class="langs-list">
            <div v-for="lang in langs" v-bind:key="lang.id" class="lang">
                <div class="card">
                    <div class="card-image waves-effect waves-block waves-light">
                        <img class="activator" :src="lang.logo">
                    </div>
                    <div class="card-content">
                        <span class="card-title activator grey-text text-darken-4">{{ lang.name }}</span>
                    </div>
                </div>
            </div>
        </div>
        <h2>Tools</h2>
        <div class="tools-list">
            <div v-for="tool in tools" v-bind:key="tool.id" class="tool">
                <div class="card">
                    <div class="card-image waves-effect waves-block waves-light">
                        <img class="activator" :src="tool.logo">
                    </div>
                    <div class="card-content">
                        <span class="card-title activator grey-text text-darken-4">{{ tool.name }}</span>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        name: 'SkillsList',
        data() {
            return {
                langs: [
                    {id: 1, name: 'PHP', logo: require("~/assets/img/php.png")},
                    {id: 2, name: 'Perl', logo: require("~/assets/img/perl.png")},
                    {id: 3, name: 'HTML5', logo: require("~/assets/img/html5.png")},
                    {id: 4, name: 'CSS3', logo: require("~/assets/img/css-3.png")}
                ],
                tools: [
                    {id: 1, name: 'Github', logo: require("~/assets/img/github.png")},
                    {id: 2, name: 'Laravel', logo: require("~/assets/img/laravel.png")},
                    {id: 3, name: 'Docker', logo: require("~/assets/img/docker.png")},
                    {id: 4, name: 'Vue.js', logo: require("~/assets/img/vue.png")},
                    {id: 5, name: 'Nuxt.js', logo: require("~/assets/img/nuxt.png")}
                ]
            }
        }
    }
</script>

<style>
    .skill-list {
        margin-top: 20px;
    }
    .langs-list {
        display: flex;
        flex-wrap: wrap;
        margin-bottom: 100px;
    }
    .lang {
        max-width: 33.3%;
        flex: 33.3%;
    }
    .tools-list {
        display: flex;
        flex-wrap: wrap;
        margin-bottom: 100px;
    }
    .tool {
        max-width: 33.3%;
        flex: 33.3%;
    }
    .card {
        width: 80%;
        margin-left: auto;
        margin-right: auto;
    }
    .card-image {
        width: 80%;
        margin-left: auto;
        margin-right: auto;
        padding-top: 10%;
    }
</style>