<template>
    <li>
        <p>Title: {{ipsum.title}}</p>
        <p>Category: {{ipsum.category}}</p>
        <p>Author: {{ipsum.author}}</p>
        <a :href="ipsum.authorUrl">Author URL</a>
        <p>Published on: {{ipsum.publishedOn}}</p>
        <!-- <p>Ipsum raw text: {{ipsum.body}}</p> -->
        <!-- <span>Ipsum text:<p v-html="ipsum.body"></p></span> -->
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
/* img {
    max-height: 15vh;
} */
p {
    font-size: 10px;
}
a {
    font-size: 10px;
}
li:hover {
    background-color: lightskyblue;
}
</style>