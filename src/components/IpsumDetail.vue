<template>
    <section v-if="ipsum">
        <span class="title">Title: {{ipsum.title}}</span>
        <span>Category: {{ipsum.category}}</span>
        <span>Author: {{ipsum.author}}</span>
        <span><a :href="ipsum.authorUrl" target="_blank">Author URL</a></span>
        <span>Published on: {{ipsum.publishedOn}}</span>
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

<style scoped>
section {
    margin-top: 12px;
}
span {
    display: inline-flex;
    flex-direction: row;
    justify-content: space-between;
    margin-left: 15px;
    color: yellow;
    font-size: 16px;
}
span.title {
    color: yellow;
}
p {
    font-size: 14px;
}
p.detail-p-tag {
    border-top: 1px solid yellow;
    color: yellow;
    margin-bottom: 40px;
    padding-top: 20px;
}
p.select-msg {
    font-size: 20px;
    font-style: italic;
    color: yellow;
    font-weight: bold;
    background-color: rgb(250, 21, 200);
    padding: 50px;
}
a {
    color: blue;
}
</style>
