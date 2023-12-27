<script>
import Nav from './Nav.vue';

export default {
    props: {
        'title': String,
        'username': String
    },
    components: { Nav }
};
</script>

<template>
    <section class="p-6 bg-gray-200">
        <header class="flex justify-between">
            <div class="flex items-center">
                <h1 class="text-2xl font">{{ title }}</h1>
                <p class="text-sm ml-4">
                    Welcome back, {{ username }}
                </p>
            </div>
            <Nav />
        </header>
    </section>

    <section class="p-6">
        <div class="max-w-xl mx-auto">
            <slot />
        </div>
    </section>
</template>
