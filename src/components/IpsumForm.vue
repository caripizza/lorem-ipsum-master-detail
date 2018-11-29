<template>
    <form @submit.prevent="onAdd(ipsum)">
        <label>
            Title:<input v-model="ipsum.title" required>
        </label>
        <label>
            Category:<input v-model="ipsum.category" required>
        </label>
        <label>
            Author:<input v-model="ipsum.author" required>
        </label>
        <br>
        <label>
            Author Url:<input v-model="ipsum.authorUrl" required>
        </label>
        <label>
            Published on:<input v-model="ipsum.publishedOn" required>
        </label>
        <label>
            Body text:<textarea cols="30" v-model="ipsum.body" required></textarea>
        </label>
        <label>
            <button type="submit">Add</button>
            <button type="button" @click="onCancel">Cancel</button>
        </label>
    </form>
</template>

<script>
export default {
    data() {
        return {
            ipsum: {
                title: '',
                category: '',
                author: '',
                authorUrl: '',
                publishedOn: '',
                body: ''
            },
            show: false
        };
    },
    props: {
        onAdd: Function,
        onCancel: Function
    }
};
</script>

<style scoped>
input, textarea {
    margin: 0px 10px 0px 10px;
}
textarea {
    margin-bottom: -6px;
    height: 40px;
}
label {
    font-size: 10px;
}
</style>