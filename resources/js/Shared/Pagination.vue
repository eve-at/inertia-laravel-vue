<script>
export default {
    props: {
        links: Array
    },
    components: { }
};
</script>

<template>
   <div>
        <Component 
            v-for="link in links"
            :is="link.url ? 'Link' : 'span'"
            :href="link.url"
            v-html="link.label"
            class="px-2"
            :class="{
                'text-gray-400': !link.url,
                'font-bold': link.active,
                'border': link.active,
                'border-white': !link.active,
                'border-gray-500': link.active
            }"
        />
    </div>
</template>
