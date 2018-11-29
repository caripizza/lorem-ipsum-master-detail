<template>
    <li>
        <p class="title">{{ipsum.title}}</p>
    </li>
</template>

<script>
export default {
    props: {
        ipsum: Object,
        onSelect: Function
    }
};
</script>

<style scoped>
li {
    background: white;
    padding: 2px;
}
li:hover {
    background-color: yellow;
}
p.title {
    margin: 2px;
    font-weight: bold;
    font-size: 20px;
    color: purple;
}
</style>
