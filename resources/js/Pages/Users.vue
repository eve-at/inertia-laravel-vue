<script>
import Layout from '../Shared/Layout.vue';

export default {
    props: {},
    components: { Link, Layout },
    props: {
        time: String
    }
};
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
