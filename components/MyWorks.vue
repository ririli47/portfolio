<template>
    <section class="works-list">
        <div v-if="show" class="infomation">
            <div class="arrow-left">
                <i class="material-icons large" v-on:click="showIdChange(-1)">navigate_before</i>
            </div>
            <div class="card">
                <div class="card-image infromation-card">
                    <a :href="works[showId].link" target="_blank"><img :src="works[showId].logo"></a>
                </div>
                <div class="card-content">
                    <dl>
                        <dt>Name</dt><dd>{{ works[showId].name }}</dd>
                        <dt>Techs</dt><dd>{{ works[showId].techs }}</dd>
                        <dt>Infomaiton</dt><dd>{{ works[showId].infomaiton }}</dd>
                    </dl>
                </div>
                <div class="card-action">
                    <a :href="works[showId].link" target="_blank">サイトへのリンク</a>
                </div>
            </div>
            <div class="arrow-right">
                <i class="material-icons large" v-on:click="showIdChange(+1)">navigate_next</i>
            </div>
        </div>

        <div v-for="work in works" v-bind:key="work.id" class="work">
            <div class="card" v-on:click="showTechs(work.id)">
                <div class="card-image waves-effect waves-block waves-light">
                    <img class="activator" :src="work.logo">
                </div>
                <div class="card-content">
                    <span class="card-title activator grey-text text-darken-4">{{ work.name }}</span>
                    <a :href="work.link" target="_blink" ><p>{{ work.name }}</p></a>
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
                    {id: 0, name: 'Tasker', link: 'https://ririli-tasker.herokuapp.com/', logo: require("~/assets/img/tasker_logo.png"),
                    techs: 'Ruby on Rails, heroku', infomaiton: 'RoRのチュートリアルを一周したのちに練習で作ったTodo管理ツール。初めてwebフレームワークを利用した成果物。'},
                    {id: 1, name: 'IdeaCafe', link: 'https://ideacafe.herokuapp.com/', logo: require("~/assets/img/ideacafe_logo.png"),
                    techs: 'Laravel, Docker, Github, heroku, PostgreSQL', infomaiton: 'PHPフレームワークであるLaravelの練習に作ったアイデアを共有するというコンセプトの簡易SNS。'},
                    {id: 2, name: 'Portfolio', link: 'https://www.ririli.net/', logo: require("~/assets/img/ririli.jpg"),
                    techs: 'Vue.js, Nuxt.js, Github, Netlify', infomaiton: 'このPortfolio。Vue.jsとNetlify使ってみたさで作成。コンポーネント指向いい。'},
                    {id: 3, name: 'AccountTimer', link: 'https://hardcore-allen-1e1019.netlify.app/', logo: require("~/assets/img/AccountTimer.png"),
                    techs: 'Vue.js, Nuxt.js, Github, Netlify', infomaiton: '長すぎる会議に嫌気が差してこんなにお金かかってるんだぞと主張するために開発。実際に会議が短くなったので神。'},
                    {id: 4, name: 'my-pallete', link: 'https://my-pallete-2acec.firebaseapp.com/', logo: require("~/assets/img/MyPalette.png"),
                    techs: 'Vue.js, Nuxt.js, Github, Firebase', infomaiton: 'よく使う色をカラーコードで保存しておくサービス。FirebaseのAuthenticationとFireStoreを使ってみたくて開発。'},
                ],
                show: false,
                showId: 0
            }
        },
        methods: {
            showTechs: function(id) {
                if(this.show && id == this.showId) {
                    this.show = !this.show
                }
                else if (!this.show) {
                    this.show = !this.show
                }
                this.showId = id
            },
            showIdChange(change) {
                this.showId = this.showId + change
                if(this.showId < 0) {
                    this.showId = this.works.length -1
                }
                else if (this.showId > this.works.length -1) {
                    this.showId = 0
                }
            }

        }
    }
</script>

<style>

    /* Material iconsを利用する */
    .material-icons {
        font-family: 'Material Icons';
        font-weight: normal;
        font-style: normal;
        font-size: 24px;  /* 推奨サイズ */
        display: inline-block;
        width: 1em;
        height: 1em;
        line-height: 1;
        text-transform: none;
        
        /* WebKitブラウザサポート */
        -webkit-font-smoothing: antialiased;
        /* Chrome、Safariサポート */
        text-rendering: optimizeLegibility;
        
        /* Firefoxサポート */
        -moz-osx-font-smoothing: grayscale;
        
        /* IEサポート */
        font-feature-settings: 'liga';
    }
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

    .infomation {
        width: 100%;
        display: flex;
        justify-content: center;
        font-size: 1rem;
    }
    .infromation-card {
        width: 20%;
        padding-top: 3%;
    }

    dl {
        font-size: 1.3rem;
        width: 100%;
        line-height: 2.5rem;
    }
    dt {
        width: 20%;
        margin-left: 5%;
        text-align: left;

    }
    dd {
        margin-left: 15%;
        margin-bottom: 3%;
        margin-right: 5%;
        text-align: left;
        border-bottom: 1px solid #42A5F5;
    }

    .arrow-left, .arrow-right {
        flex: 1;
        margin-top: 20%;
    }
    @media (max-width: 767px) {
        .topic {
            font-size: 2.1rem;
        }
        .card .card-content {
            padding-left: 0;
            padding-right: 0;
        }
        .card dl {
            font-size: 14px;
        }
        .card .card-title {
            font-size: 16px;
        }
        .arrow-left, .arrow-right {
            display: none;
        }
        a {
            font-size: 10px;
        }
    }


</style>