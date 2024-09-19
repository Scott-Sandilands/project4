<script setup>
    import { defineProps, computed} from 'vue';

    const props = defineProps({
        grades: {
            type: Array,
            required: true
        }
    });

    const average = computed(() => {
        if (props.grades.length === 0) {
            return null;
        }
        const sum = props.grades.reduce((acc, grade) => acc + grade, 0);
        return sum / props.grades.length;
    });
</script>

<template>
    <div>
        <p v-if="average !== null">Average Grade: {{ average.toFixed(2) }}</p>
        <p v-else>No grades available to calculate the average</p>
    </div>
</template>