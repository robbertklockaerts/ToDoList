<template>
    <header>
        <h1>{{ title }}</h1>
        <Button
          @btn-click="$emit('toggle-add-task')"
          :text="showAddTask ? 'Close' : 'Add Task'"
          :color="showAddTask ? 'red' : 'green'"
         
        />
        <Tasks :tasks="tasks" /> 
    </header>
</template>

<script>
import Button from './Button'

export default {
    name: 'Header',
    props: {

        title : String,

        showAddTask : Boolean
        // title: {
        // type: String,
        // default: 'Hello World',
        // }
    },
    components: {
        Button
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