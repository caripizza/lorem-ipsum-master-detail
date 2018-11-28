<template>
    <div>
      <h1>{{ msg }}</h1>
      <ul>
        <li>Header.vue List item here</li>
      </ul>
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
h3 {
    margin: 40px 0 0;
}
ul {
    list-style-type: none;
    padding: 0;
}
li {
    display: inline-block;
    margin: 0 10px;
}
a {
    color: #42b983;
}
</style>
