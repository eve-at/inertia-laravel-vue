<script setup>
import { Head, Link } from '@inertiajs/vue3';
import Layout from '../Shared/Layout.vue';
import Pagination from '../Shared/Pagination.vue';

defineProps({
    users: Object
})
</script>

<template>
    <Head>
        <title>Users</title>
    </Head>
    <Layout title="Users">
        <ul>
            <li v-for="user in users.data" :key="user.id">
                <div>{{ user.name }}</div>
                <Link :href="`/users/${user.id}/edit`">Edit</Link>
            </li>
        </ul>

        <Pagination 
            class="mt-6"
            :links="users.links" 
        />
    </Layout>
</template>
