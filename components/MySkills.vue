<template>
    <section class="skill-list">
        <div v-for="skill in skills" v-bind:key="skill.id" class="skill">
            <div class="card">
                <div class="card-image waves-block waves-light">
                    <img :src="skill.logo">
                </div>
                <div class="card-content">
                    <span class="card-title  grey-text text-darken-4">{{ skill.name }}</span>
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
                skills: [
                    {id: 1, name: 'PHP',     logo: require("~/assets/img/php.png")},
                    {id: 2, name: 'Perl',    logo: require("~/assets/img/perl.png")},
                    {id: 3, name: 'HTML5',   logo: require("~/assets/img/html5.png")},
                    {id: 4, name: 'CSS3',    logo: require("~/assets/img/css-3.png")},                    
                    {id: 5, name: 'Github',  logo: require("~/assets/img/github.png")},
                    {id: 6, name: 'Laravel', logo: require("~/assets/img/laravel.png")},
                    {id: 7, name: 'Docker',  logo: require("~/assets/img/docker.png")},
                    {id: 8, name: 'Vue.js',  logo: require("~/assets/img/vue.png")},
                    {id: 9, name: 'Nuxt.js', logo: require("~/assets/img/nuxt.png")}
                ]
            }
        }
    }
</script>

<style>
    .skill-list {
        display: flex;
        flex-wrap: wrap;
        margin-bottom: 100px;
    }
    .skill {
        max-width: 33.3%;
        flex: 33.3%;
    }
    .card {
        width: 60%;
        margin-left: auto;
        margin-right: auto;
    }
    .card-image {
        width: 60%;
        margin-left: auto;
        margin-right: auto;
        padding-top: 10%;
    }

    @media (max-width: 767px) {
        .topic {
            font-size: 2.1rem;
        }
        .card .card-content {
            padding-left: 0;
            padding-right: 0;
        }
        .card .card-title {
            font-size: 16px;
        }
    }
</style>