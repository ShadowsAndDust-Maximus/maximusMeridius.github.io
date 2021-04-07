<template>
    <header>
        <h1>{{ title }}</h1>
        <Button 
            @toggle-add-task="toggleUp"
            :text="showAddTask ? 'Close' : 'Add Task' " 
            :color="showAddTask ? 'red' : 'green'"
        />
    </header>
</template>

<script>
import Button from './Button'
export default {
    name: 'Header',
    props: {
        title: String,
        showAddTask: Boolean,
    },
    components: {
        Button,
    },
    methods: {
        toggleUp() {
            console.log(12)
            this.$emit('toggle-add-task')
        }
    }
}
</script>

<style scoped>
header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
}
</style>