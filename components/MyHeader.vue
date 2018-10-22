<template>
    <header>
        <nav class="header--menu">
            <ul>
                <li><a href="/">Home</a></li>
                <li><a href="About">About</a></li>
                <li><a href="Works">Works</a></li>
                <li><a href="Skills">Skills</a></li>
            </ul>
        </nav>
    </header>
</template>


<style>
    header {
        position: absolute;
        top: 0;
        left: 0;
        z-index: 100;
        width: 100%;
        background-color: rgba(255,255,255,0.9);
    }

    .header--menu ul {
        display: flex;
        margin: 0;
        padding: 0;
        list-style: none;
    }

    .header--menu li {
        flex: 1;
    }

    .header--menu a {
        display: block;
        padding: 15px;
        color: inherit;
        font-size: 2rem;
        text-decoration: none;
    }

    .header--menu a:hover {
        background-color: rgba(0,0,0,0.3);
    }
</style>