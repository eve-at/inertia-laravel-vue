<script>
import { Link } from '@inertiajs/vue3';
import NavLink from './NavLink.vue';

export default {
    props: {},
    components: { Link, NavLink }
};
</script>

<template>
    <nav class="ml-6">
        <ul class="flex space-x-4 list-inside">
            <li>
                <NavLink href="/" :active="$page.component === 'Home'">
                    Home
                </NavLink>            
            </li>
            <li>
                <NavLink href="/users" :active="$page.component === 'Users'">
                    Users
                </NavLink>
            </li>
            <li>
                <NavLink href="/settings" :active="$page.component === 'Settings'">
                    Settings
                </NavLink>
            </li>
            <li>
                <Link 
                    class="text-blue-500 hover:underline" href="/logout" method="post" as="button"
                >
                    Log Out
                </Link>
            </li>
        </ul>
    </nav>
</template>
