<template>
    <section class="profile">
        <img src="../assets/img/ririli.jpg" class="profile-icon">
        <dl>
            <dt>氏名</dt><dd>福原 直也</dd>
            <dt>所在地</dt><dd>東京都</dd>
            <dt>仕事内容</dt><dd>Webサービスエンジニア</dd>
            <dt>得意</dt><dd>バックエンド, フロントエンド</dd>
            <dt>苦手</dt><dd>インフラ, 運用</dd>
            <dt>興味</dt><dd>アプリ開発</dd>
        </dl>
        <div class="social">
            <a target="_brank" href="https://twitter.com/sugu_"><img src="../assets/img/Twitter.png"></a>
            <a target="_brank" href="https://qiita.com/ririli"><img src="../assets/img/qiita.png"></a>
            <a target="_brank" href="https://github.com/ririli47"><img src="../assets/img/GitHub-logo.png"></a>
        </div>
    </section>
</template>

<script>
</script>

<style scoped>
    .profile-icon {
        width: 40%;
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
        border-bottom: 1px solid red;
    }
    dd {
        margin-left: 15%;
        margin-bottom: 3%;
        text-align: left;
        border-bottom: 1px solid red;
    }
    .social {
        display: flex;
        flex-wrap: nowrap;
        justify-content: space-between;
        margin-top: 5%;
        margin-bottom: 10%;
    }
    .social a {
        flex: 1;
    }
    .social img{
        max-width: 30%;
    }

    @media (max-width: 767px) {
        dl {
            font-size: 0.8rem;
            line-height: 1.5rem;
        }
        dt {
            width: 40%;
        }
    }

</style>