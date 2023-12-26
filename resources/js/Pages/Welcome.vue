<script>
export default {
    props: {
        name: {
            type: String
        },
        frameworks: {
            type: Array
        }
    }
};
</script>

<template>
    <h1>Hello, {{ name }}</h1>

    <p>In this series, we'll use the following frameworks:</p>

    <ul>
        <li v-for="framework in frameworks" v-text="framework"></li>
    </ul>
</template>
