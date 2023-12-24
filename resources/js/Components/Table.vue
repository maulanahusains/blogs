<script setup>
    import { Link } from '@inertiajs/vue3';
</script>

<template>
    <table class="w-full">
        <thead class="text-left">
            <tr class="text-gray-700  border border-transparent border-b-gray-400">
                <slot name="thead">
                    <th class="p-4">#</th>
                    <th class="p-4">Name</th>
                    <th class="p-4">Username</th>
                    <th class="p-4">Action</th>
                </slot>
            </tr>
        </thead>
        <tbody class="text-left">
            <slot name="tbody">
                <tr class="border border-transparent border-b-gray-300">
                    <th class="p-4">1</th>
                    <td class="p-4">Husen</td>
                    <td class="p-4">MaulHusein</td>
                    <td class="p-4">
                        <Link>Cuk</Link>
                        <Link>Wow</Link>
                    </td>
                </tr>
            </slot>
        </tbody>
    </table>
</template>

