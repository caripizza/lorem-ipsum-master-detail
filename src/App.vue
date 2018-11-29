<template>
    <div id="app">
    <Header msg="Lorem Ipsum app"/>
    <Ipsums 
        :ipsums="ipsums"
        :onSelect="handleSelect"/>
    <IpsumDetail 
        :ipsum="selected"/>
    </div>
</template>

<script>
import ipsumsApi from './services/ipsumsApi.js';
import Header from './components/Header';
import Ipsums from './components/Ipsums';
import IpsumDetail from './components/IpsumDetail';

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
        Ipsums,
        IpsumDetail
    },
    methods: {
        handleSelect(ipsum) {
            this.selected = ipsum === this.selected ? null : ipsum;
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
