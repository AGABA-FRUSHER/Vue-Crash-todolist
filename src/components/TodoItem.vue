<template>
    <div class="todo-item" v-bind:class="{'is-complete':completed}">
        <p>
            <input type="checkbox" @change="markComplete">
            {{todo.title}}
            <button @click="$emit('del-todo', todo.id)" class="del">x </button>
            </p>
    </div>
</template>


<script>
export default {
    name: "TodoItem",
    props: ['todo'],
    data() {
        return {
            completed: false
        }
    },
    created() {
        this.completed = this.todo.completed
    },
    methods:{
        markComplete() {
            this.completed = !this.completed
            console.log(!this.todo.completed)
        }
    }
    
}
</script>



<style scoped>
.todo-item{
    background-color: green;
    padding: 10px;
    border-bottom: 1px aliceblue dotted; 
    
}
.is-complete {
    text-decoration: line-through;
}
.del {
    background-color: darkred;
    color:azure;
    border: none;
    padding: 5px 9px;
    border-radius: 50%;
    cursor: pointer;
    float: right;
}

</style>