<template>
    <IpsumDetail v-bind:ipsum="ipsum"/>
</template>

<script>
import IpsumDetail from './IpsumDetail';

export default {
    props: {
        ipsum: Object
    },
    components: {
        IpsumDetail
    }
};
</script>

<style scoped>

</style>