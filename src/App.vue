<script setup>
  import GradeInput from './components/GradeInput.vue'
  import GradeList from './components/GradeList.vue'
  import GradeAverage from './components/GradeAverage.vue'
</script>

<template>
  <div>
    <h1>Grade Manager</h1>
    <GradeInput></GradeInput>
    <GradeList></GradeList>
    <GradeAverage></GradeAverage>
  </div>
</template>