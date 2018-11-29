<template>
    <section>
        <IpsumList 
            v-bind:ipsums="ipsums"
            v-bind:onSelect="handleSelect"/>
        <Ipsum v-bind:ipsum="selected"/>
    </section>
</template>

<script>
import ipsumsApi from '../services/ipsumsApi';
import Ipsum from './Ipsum';
import IpsumList from './IpsumList';

export default {
    data() {
        return {
            ipsums: ipsumsApi.getIpsums(),
            selected: null
        };
    },
    components: {
        Ipsum,
        IpsumList
    },
    methods: {
        handleSelect(ipsum) {
            this.selected = ipsum === this.selected ? null : ipsum;
            console.log(ipsum.title);
        }
    }
};
</script>

<style scoped>
section {
    height: 30vh;
    overflow: auto;
    border: 2px solid red;
}
/* width */
::-webkit-scrollbar {
    width: 12px;
}
/* Track */
::-webkit-scrollbar-track {
    background: yellow; 
}
/* Handle */
::-webkit-scrollbar-thumb {
    background: #888; 
}
/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
    background: #555; 
}
ul {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-gap: 4px;
    /* display: flex;
    flex-direction: row; */
    /* overflow: auto; */
    list-style: none;
    padding: 0;
    margin: 0;
    /* height: 50vh; */
}
</style>
