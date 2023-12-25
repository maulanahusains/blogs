<script setup>
    import { Link } from '@inertiajs/vue3';
    const props = defineProps({
        link: String,
    });
</script>

<template>
    <Link :href="link" class="py-2 px-8"><slot></slot></Link>
</template>