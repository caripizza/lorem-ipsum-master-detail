<template>
    <div>
        <img alt="Bob Ross logo" src="../assets/logo.png">
        <h1>{{ msg }}</h1>
    </div>
</template>

<script>
export default {
    name: 'Header',
    props: {
        msg: String
    }
};
</script>

<style scoped>
div {
  background: red;
}
h1 {
    margin: 0 auto;
    color: yellow;
}
img {
    width: 10%;
}
</style>
