<template>
    <section v-if="ipsum">
        <span>Ipsum text:<p v-html="ipsum.body"></p></span>
    </section>
    <section v-else>
        Please select an ipsum
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
img {
    max-height: 25vh;
}
p {
    font-size: 10px;
}
</style>
