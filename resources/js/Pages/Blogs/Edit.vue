<script setup>
    import Master from '../../Components/Layouts/Master.vue';
    import Card from '../../Components/Card.vue';
    import Input from '../../Components/Input.vue';

    import { Link } from '@inertiajs/vue3';

</script>

<template>
    <Master>
        <template #content>
            <Card>
                <template #card-content>
                    <h1 class="font-bold text-xl">Create Blog</h1>
                    <form action="">
                        <div class="flex flex-col mt-4">
                            <label for="">Title</label>
                            <Input type="text" id="title" />
                        </div>
                        <div class="flex flex-col my-4">
                            <label for="">Content</label>
                            <textarea name="" id="" cols="30" rows="5" class="p-4 border rounded-lg border-gray-300 focus:border-black focus:outline-none"></textarea>
                        </div>
                        <button type="submit" class="text-base bg-green-500 text-white hover:bg-green-600 px-8 py-2 rounded-lg">Create</button>
                    </form>
                </template>
            </Card>
        </template>
    </Master>
</template>