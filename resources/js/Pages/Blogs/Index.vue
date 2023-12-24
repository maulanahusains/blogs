<script setup>
    import Master from '../../Components/Layouts/Master.vue';
    import Table from '../../Components/Table.vue';
    import Card from '../../Components/Card.vue';

    import { Link } from '@inertiajs/vue3';

    const props = defineProps({
        blogs: Object
    });
</script>

<template>
    <Master>
        <template #content>
            <Card>
                <template #card-content>
                    <div class="flex items-center justify-between">
                        <h1 class="font-bold text-xl">Blog index</h1>
                        <Link class="bg-slate-400 text-white py-1 px-2 rounded-lg hover:bg-slate-500">New Data</Link>
                    </div>
                    <Table>
                        <template #thead>
                            <th class="p-4">#</th>
                            <th class="p-4">Title</th>
                            <th class="p-4">Content</th>
                            <th class="p-4">Action</th>
                        </template>
                        <template #tbody>
                            <tr v-for="data, i in blogs">
                                <th class="p-4">{{ i + 1 }}</th>
                                <td class="p-4">{{ data.title }}</td>
                                <td class="p-4">{{ (data.content).slice(0, 30) }}......</td>
                                <td class="p-4">
                                    <Link class="bg-blue-500 text-white py-2 px-2 rounded-lg hover:bg-blue-600">See Detail</Link>
                                </td>
                            </tr>
                        </template>
                    </Table>
                </template>
            </Card>
        </template>
    </Master>
</template>