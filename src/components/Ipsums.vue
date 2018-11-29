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
}
ul {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-gap: 10px;
    /* display: flex;
    flex-direction: row; */
    /* overflow: auto; */
    list-style: none;
    background-color: lightcoral;
    padding-left: 0;
    /* height: 50vh; */
}
</style>
