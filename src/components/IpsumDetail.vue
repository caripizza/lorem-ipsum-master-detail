<template>
    <section v-if="ipsum">
        <p v-html="ipsum.body"></p>
    </section>
    <section v-else>
        <p class="select-msg">Please select an ipsum!</p>
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
/* img {
    max-height: 25vh;
} */
p {
    font-size: 10px;
}
p.select-msg {
    font-size: 20px;
    font-style: italic;
    color: purple;
    font-weight: bold;
    background-color: green;
    padding: 50px;
}
</style>
