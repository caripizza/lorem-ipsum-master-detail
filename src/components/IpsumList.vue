<template>
    <ul>
        <IpsumItem v-for="ipsum in ipsums"
            @click.native="onSelect(ipsum)"
            :key="ipsum.title"
            :ipsum="ipsum"/>
    </ul>
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

<style>

</style>
