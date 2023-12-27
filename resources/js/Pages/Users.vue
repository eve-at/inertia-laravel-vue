<script>
import { Link } from '@inertiajs/vue3';
import Nav from '../Shared/Nav.vue';

export default {
    props: {},
    components: { Nav, Link },
    props: {
        time: String
    }
};
</script>

<template>
    <h1 class="text-4xl font bold">Users</h1>

    <Nav />

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
</template>
