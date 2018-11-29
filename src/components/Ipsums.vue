<template>
    <section>
    <ul>
        <Ipsum v-for="ipsum in ipsums"
            @click.native="onSelect(ipsum)"
            :key="ipsum.title"
            :ipsum="ipsum"/>
    </ul>
    </section>
</template>

<script>
import Ipsum from './Ipsum';

export default {
    props: {
        ipsums: Array,
        onSelect: Function
    },
    components: {
        Ipsum
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
