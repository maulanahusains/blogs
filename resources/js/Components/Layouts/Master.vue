<script setup>
    import sidebar from './Sidebar.vue';
    import CardVue from '../Card.vue';
    import Table from '../Table.vue';
</script>

<template>
    <div class="flex">
        <sidebar />
        <div class="p-8 w-full flex flex-col gap-6">
            <slot name="content">
                <CardVue>
                    <template #card-content>
                        <Table>
                            
                        </Table>
                    </template>
                </CardVue>
            </slot>
        </div>
    </div>
</template>