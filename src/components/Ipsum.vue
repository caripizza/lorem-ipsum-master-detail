<template>
    <section>
        <IpsumForm :onAdd="handleAdd"/>
        <IpsumDetail :ipsum="ipsum"/>
    </section>
</template>

<script>
import IpsumDetail from './IpsumDetail';
import IpsumForm from './IpsumForm';

export default {
    props: {
        ipsum: Object
    },
    components: {
        IpsumDetail,
        IpsumForm
    },
    methods: {
        handleAdd(ipsum) {
            console.log('you want to add', JSON.stringify(ipsum));
        }
    }
};
</script>

<style scoped>

</style>