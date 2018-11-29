<template>
    <li>
        <p class="title">{{ipsum.title}}</p>
        <p>Category: {{ipsum.category}}</p>
        <p>Author: {{ipsum.author}}</p>
        <a :href="ipsum.authorUrl" target="_blank">Author URL</a>
        <p>Published on: {{ipsum.publishedOn}}</p>
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
p {
    font-size: 12px;
    margin: 2px;
    color: purple;
}
p.title {
    font-weight: bold;
    font-size: 20px;
    /* margin: 0 auto; */
    color: purple;
}
a {
    font-size: 12px;
}
</style>
