<template>
    <section class="profile">
        <img src="../assets/img/ririli.jpg" class="profile-icon">
        <dl>
            <dt>氏名：</dt><dd>福原 直也</dd>
            <dt>所在地：</dt><dd>東京都</dd>
            <dt>仕事内容：</dt><dd>webバックエンド開発</dd>
        </dl>
        <div class="social">
            <img src="../assets/img/Twitter.png">
            <img src="../assets/img/Twitter.png">
            <img src="../assets/img/Twitter.png">
        </div>
    </section>
</template>

<script>
</script>

<style>
    .profile-icon {
        width: 80%;
    }
    dl {
        font-size: 1.3rem;
        width: 100%;
    }
    dt {
        float: left;
        width: 50%;
        margin-left: 5%;
        text-align: left;
    }
    dd {
        margin-left: 80px;
        text-align: left;
    }
    .social {
        display: flex;
        flex-wrap: nowrap;
    }
    .social img{
        max-width: 33.3%;
        margin-top: auto;
        margin-bottom: auto;
        flex: 30%;
    }
</style>