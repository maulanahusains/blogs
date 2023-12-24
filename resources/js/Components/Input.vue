<script setup>
    import { ref } from 'vue';
    defineProps({
        type: String,
        id: String
    });
    const val = ref('');
</script>

<template>
    <input :type="type" class="w-full h-10 rounded-md border" :class="[
        type == 'text' || type == 'password' ? 'p-4 border-gray-300 focus:border-black focus:outline-none'
        : type == 'date' ? 'px-4' : 'none'
        ]" v-model="val" @input="$emit('inputData', {val, id})"/>
</template>

<!-- Contoh penggunaann di parent -->

<!-- <script setup>
    const cuk = ref({});
    function getData(data) {
        cuk.value[data.id] = data.val;
    }
</script> -->

<!-- <template>
    <Input type="text" id="nahkan" @inputData="getData"/>
    <Input type="text" id="nahkancuk" @inputData="getData"/>
    <p v-for="childVal, c in Object.values(cuk)" :key="childVal" :id="c">{{ childVal }}</p>
</template> -->