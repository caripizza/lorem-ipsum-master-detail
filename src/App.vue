<template>
    <div id="app">
    <Header msg="Lorem Ipsum app"/>
        <!-- {{ipsums[0]}} -->
    <Ipsums v-bind:ipsums="ipsums"/>
    </div>
</template>

<script>
import ipsumsApi from './services/ipsumsApi.js';
import Header from './components/Header.vue';
import Ipsums from './components/Ipsums';

export default {
    name: 'app',
    data() {
        return {
            ipsums: ipsumsApi.getIpsums(),
        };
    },
    components: {
        Header,
        Ipsums
    }
};
</script>

<style>
#app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin: 0 auto;
}
html {
    background: red;
}
</style>
