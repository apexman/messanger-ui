<template>
    <div id="app">
        <div id="nav">
            <MainPage></MainPage>
        </div>
        <router-view/>
    </div>
</template>

<script>
    import MainPage from "./components/MainPage";

    export default {
        components: {MainPage}
    }
</script>

<style>
    html, body {
        height: 100%;
    }

    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        height: 100%;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
    }

    #nav {
        height: 100%;
    }

    #nav a {
        font-weight: bold;
        color: #2c3e50;
    }

    #nav a.router-link-exact-active {
        color: #42b983;
    }
</style>