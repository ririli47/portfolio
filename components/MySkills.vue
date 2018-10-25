<template>
    <section class="skill-list">
        <h2>Languages</h2>
        <div class="langs-list">
            <div v-for="lang in langs" v-bind:key="lang.id">
                <div class="card">
                    <div class="card-image waves-effect waves-block waves-light">
                        <img class="activator" :src="lang.logo">
                    </div>
                    <div class="card-content">
                        <span class="card-title activator grey-text text-darken-4">{{ lang.name }}<i class="material-icons right">more_vert</i></span>
                        <p><a href="#">ここがりんくだよ</a></p>
                    </div>
                    <div class="card-reveal">
                        <span class="card-title grey-text text-darkens-4">{{ lang.name }}<i class="material-icons right">close</i></span>
                        <p>これはせつめいだよ</p>
                    </div>
                </div>
            </div>
        </div>
        <h2>Tools</h2>
        <div class="tools-list">
            <div v-for="tool in tools" v-bind:key="tool.id">
                <div class="card">
                    <div class="card-image waves-effect waves-block waves-light">
                        <img class="activator" :src="tool.logo">
                    </div>
                    <div class="card-content">
                        <span class="card-title activator grey-text text-darken-4">{{ tool.name }}<i class="material-icons right">more_vert</i></span>
                        <p><a href="#">ここがりんくだよ</a></p>
                    </div>
                    <div class="card-reveal">
                        <span class="card-title grey-text text-darkens-4">{{ tool.name }}<i class="material-icons right">close</i></span>
                        <p>これはせつめいだよ</p>
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
                    //?????????
                    {id: 1, name: 'PHP', logo: ''},
                    {id: 2, name: 'HTML5', logo: ''},
                    {id: 3, name: 'CSS3', logo: ''}
                ],
                tools: [
                    //?????????
                    {id: 1, name: 'Github', logo: ''},
                    {id: 2, name: 'Vue.js', logo: ''},
                    {id: 3, name: 'Nuxt.js', logo: ''}
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
        margin-top: 20px;
    }
    .tools-list {
        display: flex;
        margin-top: 20px;
    }
    .card {
        flex: 1;
        margin: 20px;
    }
    .card-image {
        align-items: center;
        width: 100%;
    }
</style>