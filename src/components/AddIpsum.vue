<template>
    <div class="if">
    <div v-if="!show">
        <button @click="show = true">Add an Ipsum</button>
    </div>
    <div v-else class="else">
        <h3>Add a new Ipsum</h3>
        <IpsumForm
            :onAdd="handleAdd"
            :onCancel="() => show = false"/>
    </div>
    </div>
</template>

<script>
import IpsumForm from './IpsumForm';

export default {
    data() {
        return {
            show: false
        };
    },
    components: {
        IpsumForm
    },
    props: {
        onAdd: Function
    },
    methods: {
        handleAdd(ipsum) {
            this.show = false;
            this.onAdd(ipsum);
        }
    }
};
</script>

<style scoped>
div {
    color: yellow;
}
div.if {
    height: 75%;
    margin-top: 10px;
}
h3 {
    margin: 0;
}
</style>