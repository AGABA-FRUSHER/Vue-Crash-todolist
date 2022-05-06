<template>
    <div>
        <button v-on:click="updateTitle">Update  Title</button>
    </div>
</template>


<script>
export default {
    name: 'ChildComponent',

    methods:{
        updateTitle() {
            this.$emit('changeTitle', 'I need to learn this asap')
        }
    }
}
</script>



<style scoped>

</style>
