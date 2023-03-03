<script setup>
import { Head, Link } from '@inertiajs/vue3';

defineProps({
    canLogin: Boolean,
    canRegister: Boolean,
    laravelVersion: String,
    phpVersion: String,
});
</script>

<template>

              <Link
                    :href="route('logout')"
                    method="post"
                    as="button"
                    class="tw-underline tw-text-sm tw-text-gray-600 hover:tw-text-gray-900 tw-rounded-md focus:tw-outline-none focus:tw-ring-2 focus:tw-ring-offset-2 focus:tw-ring-indigo-500"
                    >Log Out</Link
                >

<div id="component-root" class="tw-block lg:tw-relative lg:tw-w-[90vw] lg:tw-bg-gray-300 lg:tw-mx-auto">

<div id="section-1" class="lg:tw-h-[150px] lg:tw-w-[95%] lg:tw-bg-red-100">
     <img src="/assets/organization-logo.png" class="lg:tw-w-[100px] lg:tw-m-3">
     <span class="lg:tw-text-[40px]">Kagoshima Wonderful Walk</span>
     <div class="lg:tw-text-[30px] lg:tw-m-[10px]">Walk and talk with the locals!!!!!!!!!</div>
</div>

<div id="section-2" class="lg:tw-h-[450px] lg:tw-w-[95%] lg:tw-bg-red-500 lg:tw-overflow-hidden">
     <img src="/assets/kagoshima_panorama.jpg" class="lg:tw-h-[500px] lg:tw-mx-[-75px]">
</div>

<div id="section-3" class="lg:tw-h-[100px] lg:tw-w-[95%] lg:tw-bg-red-100">
    <div class="lg:tw-text-[30px]">We will guide you in the charms of Kagoshima in English.</div>
    <div class="lg:tw-text-[30px]">We will guide you in the charms of Kagoshima in English.</div>
</div>

<div id="section-side" class="lg:tw-absolute lg:tw-inset-y-0 lg:tw-right-0 lg:tw-h-[700px] lg:tw-w-[250px] lg:tw-bg-gray-100 lg:tw-p-4 lg:tw-bg-orange-100">
<div id="nav-row" class="tw-">
    <img src="/assets/nav-sakurajima.png" class="lg:tw-w-[60px] lg:tw-m-1">
    <img src="/assets/nav-culture.png" class="lg:tw-w-[60px] lg:tw-m-1">
    <img src="/assets/nav-samurai.png" class="lg:tw-w-[60px] lg:tw-m-1">
</div>
<v-text-field label="search" v-model="search"></v-text-field>

<div v-if="canLogin" class="sm:fixed sm:top-0 sm:right-0 p-6 text-right">
    <Link
        v-if="$page.props.auth.user"
        :href="route('dashboard')"
        class="font-semibold text-gray-600 hover:text-gray-900 dark:text-gray-400 dark:hover:text-white focus:outline focus:outline-2 focus:rounded-sm focus:outline-red-500"
        >Dashboard</Link>
    <div v-else>
        <Link
            :href="route('login')"
            class="font-semibold text-gray-600 hover:text-gray-900 dark:text-gray-400 dark:hover:text-white focus:outline focus:outline-2 focus:rounded-sm focus:outline-red-500"
            >Log in</Link>
        <Link
            v-if="canRegister"
            :href="route('register')"
            class="ml-4 font-semibold text-gray-600 hover:text-gray-900 dark:text-gray-400 dark:hover:text-white focus:outline focus:outline-2 focus:rounded-sm focus:outline-red-500"
            >Register</Link
        >
    </div>
</div>

<div id="news-field">news feed</div>
</div>

<div id="section-5" class="lg:tw-bottom-0 lg:tw-flex lg:tw-flex-wrap tw-min-w-[90%] lg:tw-justify-between lg:tw-m-5 lg:tw-w-[70%]">
    <img src="/assets/nav-sakurajima.png" class="lg:tw-w-[240px] lg:tw-m-3">
    <img src="/assets/nav-culture.png" class="lg:tw-w-[240px] lg:tw-m-3">
    <img src="/assets/nav-samurai.png" class="lg:tw-w-[240px] lg:tw-m-3">
    <img src="/assets/nav-samurai.png" class="lg:tw-w-[240px] lg:tw-m-3">
</div>

</div>

</template>