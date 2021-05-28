<template>
    <div id="app">
        <world-map id="map"></world-map>
    </div>
</template>

<script>
/* eslint-disable */
import worldMap from "./components/map.vue";
export default {
    name: 'App',
    components: {
        worldMap
    },
    data() {
        return {
        };
    },
    methods: {

    }
}
</script>

<style>
#app {
    border: 1px solid #ccc;
    width: 100vw;
    height: 100vh;
}
</style>
