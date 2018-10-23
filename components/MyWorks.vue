<template>
    <section class="works-list">
        <div v-for="work in works" v-bind:key="work.id">
            <div class="card">
                <div class="card-image waves-effect waves-block waves-light">
                    <img class="activator" :src="work.logo">
                </div>
                <div class="card-content">
                    <span class="card-title activator grey-text text-darken-4">{{ work.name }}<i class="material-icons right">more_vert</i></span>
                    <p><a href="#">ここがりんくだよ</a></p>
                </div>
                <div class="card-reveal">
                    <span class="card-title grey-text text-darken-4">{{ work.name }}<i class="material-icons right">close</i></span>
                    <p>これはせつめいだよ</p>
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
                    {id: 1, name: 'Tasker', logo: 'img/tasker_logo.svg'},
                    {id: 2, name: 'IdeaCafe', logo: 'img/ideacafe_logo.png'}
                ]
            }
        }
    }
</script>

<style>
    .works-list {
        display: flex;
    }
    .card {
        flex: 1;
        margin: 20px; 
    }
</style>