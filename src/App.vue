<template>
    <div id="app">
      <img alt="Vue logo" src="./assets/logo.png">
      <HelloWorld msg="Hi from App.vue"/>
      {{ipsums}}
    </div>
</template>

<script>
import ipsumsApi from './services/ipsumsApi.js';
import HelloWorld from './components/HelloWorld.vue';


export default {
    name: 'app',
    data() {
        return {
            ipsums: ipsumsApi.getIpsums(),
        };
    },
    components: {
        HelloWorld
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
