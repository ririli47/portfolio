<template>
    <header>
        <nav class="header--menu pink">
            <ul>
                <li><router-link to="/">Home</router-link></li>
                <li><router-link to="/About">About</router-link></li>
                <li><router-link to="/Works">Works</router-link></li>
                <li><router-link to="/Skills">Skills</router-link></li>
            </ul>
        </nav>
    </header>
</template>


<style>
    header {
        position: fixed;
        top: 0;
        left: 0;
        z-index: 100;
        width: 100%;
    }

    .header--menu ul {
        display: flex;
        margin: 0;
        padding: 0;
        list-style: none;
    }

    .header--menu li {
        flex: 1;
        margin-bottom: 10px;
    }

    .header--menu a {
        display: block;
        color: inherit;
        font-size: 2rem;
        text-decoration: none;
    }

    .header--menu a:hover {
        background-color: rgba(0,0,0,0.3);
    }
</style>