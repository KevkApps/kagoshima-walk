<script setup>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import { Head, Link } from '@inertiajs/vue3';

</script>

<template>
<div>
<div>DASHBOARD</div>

        <Link
            :href="route('logout')"
            method="post"
            class="tw-font-semibold tw-text-gray-600 hover:tw-text-gray-900 dark:tw-text-gray-400 dark:hover:tw-text-white focus:tw-outline focus:tw-outline-2 focus:tw-rounded-sm focus:tw-outline-red-500"
            >Logout</Link>

        </div>
</template>