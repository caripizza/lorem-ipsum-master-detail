<template>
    <div id="app">
    <Header msg="Lorem Ipsum app"/>
        <!-- {{ipsums[0]}} -->
    <Ipsums 
        :ipsums="ipsums"
        :onSelect="handleSelect"/>
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
            selected: null
        };
    },
    components: {
        Header,
        Ipsums
    },
    methods: {
        handleSelect(ipsum) {
            this.selected = ipsum;
            console.log(ipsum.title);
        }
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
