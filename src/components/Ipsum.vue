<template>
    <li>
        <p>Title:{{ipsum.title}}</p>
        <p>Category:{{ipsum.category}}</p>
        <p>Author:{{ipsum.author}}</p>
        <p>Author URL:{{ipsum.authorUrl}}</p>
        <p>Published on:{{ipsum.publishedOn}}</p>
        <p>Ipsum text:{{ipsum.body}}</p>
    </li>
</template>

<script>
export default {
    props: {
        ipsum: Object
    }
};
</script>

<style scoped>
li {
    border: 2px solid blue;
    background: white;
}
</style>
