<template>
    <section v-if="ipsum">
        <p v-html="ipsum.body" class="detail-p-tag"></p>
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
    font-size: 18px;
}
p.detail-p-tag {
    color: yellow;
}
p.select-msg {
    font-size: 20px;
    font-style: italic;
    color: purple;
    font-weight: bold;
    background-color: rgb(250, 21, 200);
    padding: 50px;
}
</style>
