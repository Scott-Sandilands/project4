<script setup>
  import GradeInput from './components/GradeInput.vue'
  import GradeList from './components/GradeList.vue'
  import GradeAverage from './components/GradeAverage.vue'
  
  import {ref} from 'vue';

  const grades = ref([]);

  const addGrade = (gradeData) => {
    if (!isNaN(gradeData.amount)) {
      grades.value.push(gradeData.amount);
    }
  };

  const deleteGrade = (index) => {
    grades.value.splice(index,1);
  };


</script>

<template>
  <div>
    <h1>Grade Manager</h1>
    <GradeInput @gradeSubmitted="addGrade" />
    <GradeList :grades="grades" @deleteGrade="deleteGrade" />
    <GradeAverage :grades="grades" />
  </div>
</template>