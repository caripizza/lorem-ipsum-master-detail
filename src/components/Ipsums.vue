<template>
    <ul>
        I am Ipsums.vue
        <Ipsum v-for="ipsum in ipsums"
        v-bind:key="ipsum.title"
        v-bind:ipsum="ipsum"/>
    </ul>
</template>

<script>
import Ipsum from './Ipsum';

export default {
    props: {
        ipsums: Array
    },
    components: {
        Ipsum
    }
};
</script>

<style scoped>
ul {
    list-style: none;
    background-color: lightcoral;
    padding-left: 0;
}
</style>
