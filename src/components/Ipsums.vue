<template>
    <section>
        <IpsumList 
            :ipsums="ipsums"
            :onSelect="handleSelect"/>
        <Ipsum :ipsum="selected"/>
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
        IpsumList,
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
    height: 20vh;
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
</style>
