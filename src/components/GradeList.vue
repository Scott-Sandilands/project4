<script setup>

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