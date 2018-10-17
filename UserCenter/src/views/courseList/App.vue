<template>
    <div id="app">
        <!-- <img src="@/assets/logo.png"> -->
        this is page couser_list
        <Process />
        <Course />

    </div>
</template>

<script>
import Process from './components/Process';
import Course from './components/Course';

export default {
    name: 'App',
    components: {
        Process,
        Course,
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
