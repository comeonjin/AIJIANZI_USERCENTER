<template>
    <div id="app">
        <!-- <img src="@/assets/logo.png"> -->
        this is page couser_list
        <Process />

    </div>
</template>

<script>
import Process from './components/Process';

export default {
    name: 'App',
    components: {
        Process,
    },
};
</script>

<style>
#app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    /* margin-top: 60px; */
}
</style>
