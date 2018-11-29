<template>
    <section>
        <div v-if="!show">
            <button @click="show = true">Click to Add an Ipsum</button>
        </div>
        <div v-else>
            <h2>Add an Ipsum</h2>
            <form @submit.prevent="handleSubmit">
                <label>
                    Title:<input v-model="ipsum.title" required>
                </label>
                <label>
                    Category:<input v-model="ipsum.category" required>
                </label>
                <label>
                    Author:<input v-model="ipsum.author" required>
                </label>
                <label>
                    Author Url:<input v-model="ipsum.authorUrl" required>
                </label>
                <label>
                    Published on:<input v-model="ipsum.publishedOn" required>
                </label>
                <label>
                    Body text:<input v-model="ipsum.body" required>
                </label>
                <label>
                    <button>Add</button>
                </label>
            </form>
        </div>
    </section>
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
        onAdd: Function
    },
    methods: {
        handleSubmit() {
            this.onAdd(this.ipsum);
        }
    }
};
</script>

<style scoped>
section {
    background-color: lightblue;
}
</style>