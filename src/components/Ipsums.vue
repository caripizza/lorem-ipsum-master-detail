<template>
    <ul>
        I am Ipsums.vue
        <Ipsum/>
    </ul>
</template>

<script>
import Ipsum from './Ipsum';

export default {
    components: {
        Ipsum
    }
};
</script>

<style>
ul {
    list-style: none;
}
</style>
