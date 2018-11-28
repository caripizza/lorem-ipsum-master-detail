<template>
    <section v-if="ipsum">
        I am IpsumDetail.vue
        {{ipsum.title}}
    </section>
</template>

<script>
export default {
    props: {
        ipsum: Object
    }
};
</script>

<style>

</style>
