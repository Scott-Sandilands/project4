<script setup>
    import {ref, defineEmits} from 'vue';

    const Grade = ref('');

    const emit = defineEmits([ 'gradeSubmitted' ]);

    const onSubmit = () =>{
        const gradeData = {
            amount: parseFloat(grade.value),
        };

        emit('gradeSubmitted', gradeData);

        grade.value = '';
    };
</script>

<template>
    <div>
        <input v-model="grade" type="number" placeholder="Enter a grade" />
        <button @click="onSubmit">Add Grade</button>
    </div>
</template>