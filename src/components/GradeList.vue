<script setup>
    import { defineProps, defineEmits } from 'vue';

    const props = defineProps({
        grades: {
            type: Array,
            required: true
        }
    });

    const emit = defineEmits(['deleteGrade']);

    const deleteGrade = (index) => {
        emit('deleteGrade', index);
    };

</script>

<template>
    <div>
        <ul>
            <li v-for="(grade, index) in grades" :key="index">
                {{ grade }} <button @click="$emit('delete-grade', index)">Delete</button>
            </li>
        </ul>
    </div>
</template>