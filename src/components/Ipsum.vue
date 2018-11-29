<template>
    <section>
        <IpsumDetail :ipsum="ipsum"/>
        <!-- <IpsumForm :onAdd="handleAdd"
            :onCancel="() => show = false"/> -->
    </section>
</template>

<script>
import IpsumDetail from './IpsumDetail';
// import IpsumForm from './IpsumForm';

export default {
    props: {
        ipsum: Object
    },
    components: {
        IpsumDetail,
        // IpsumForm
    },
    // methods: {
    //     handleAdd(ipsum) {
    //         this.ipsums.push(ipsum);
    //     }
    // }
};
</script>

<style scoped>

</style>