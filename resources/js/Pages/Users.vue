<script setup>
import { Head, Link } from '@inertiajs/vue3';
import Layout from '../Shared/Layout.vue';

defineProps({
    time: String,
    users: Array
})
</script>

<template>
    <Head>
        <title>Users</title>
    </Head>
    <Layout title="Users">
        <ul>
            <li v-for="user in users" :key="user.id" v-text="user.name"></li>
        </ul>
    </Layout>
</template>
