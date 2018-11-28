<template>
    <div id="app">
      <img alt="Vue logo" src="./assets/logo.png">
      <Header msg="Lorem Ipsum app"/>
      raw ipsum[0] > {{ipsums[0]}}
    </div>
</template>

<script>
import ipsumsApi from './services/ipsumsApi.js';
import Header from './components/Header.vue';


export default {
    name: 'app',
    data() {
        return {
            ipsums: ipsumsApi.getIpsums(),
        };
    },
    components: {
        Header
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
    margin-top: 60px;
}
</style>
