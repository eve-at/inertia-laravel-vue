<script>
import Nav from './Nav.vue';

export default {
    props: {
        'title': String
    },
    components: { Nav }
};
</script>

<template>
    <section class="p-6 bg-gray-200">
        <header class="flex justify-between">
            <h1 class="text-2xl font" >{{ title }}</h1>
            <Nav />
        </header>
    </section>

    <section class="p-6">
        <div class="max-w-xl mx-auto">
            <slot />
        </div>
    </section>
</template>
