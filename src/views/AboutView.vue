<template>
  <div class="about">
    <p>{{ title }}</p>
    <Child v-on:changeTitle="updateTitleText" /> 
  </div>
</template>


<script>
import Child from '@/components/Child'
export default {
  name:'AboutView',
  components: {
    Child,
  },
  data() {
   return{ title : 'Welcome to Vue'}
  },
  methods: {
  
    updateTitleText(title) {
      this.title = title
    }

  }
  

}
</script>


<style scoped>

</style>
