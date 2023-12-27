<script setup>
import { Link } from '@inertiajs/vue3';
import Layout from '../Shared/Layout.vue';

defineProps({
    time: String
})
</script>

<template>
    <Layout title="Users">
        <div style="margin-top: 800px;">
            <p>The current time is {{ time  }}</p>
        </div>

        <Link 
            href="/users" 
            class="text-blue-500 hover:underline"
            preserve-scroll
        >
            Refresh
        </Link>
    </Layout>
</template>
