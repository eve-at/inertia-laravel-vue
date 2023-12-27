<script>
import Layout from '../Shared/Layout.vue'

export default {
    props: {
        'username': String
    },
    components: { Layout }
};
</script>

<template>
    <Layout 
        :username="username"
        title="Home"
    >
        Hello there
    </Layout>
</template>
