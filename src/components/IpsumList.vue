<template>
    <section>
    <ul>
        <IpsumItem v-for="ipsum in ipsums"
            @click.native="onSelect(ipsum)"
            :key="ipsum.title"
            :ipsum="ipsum"/>
    </ul>
    </section>
</template>

<script>
import IpsumItem from './IpsumItem';

export default {
    props: {
        ipsums: Array,
        onSelect: Function
    },
    components: {
        IpsumItem
    }
};
</script>

<style scoped>
section {
    overflow: auto;
}
ul {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 4px;
    list-style: none;
    padding: 0;
    margin: 0;
}
</style>
