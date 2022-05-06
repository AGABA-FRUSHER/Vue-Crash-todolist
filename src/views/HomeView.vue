<template>
  <div class="home">

    <!-- <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <div>
      <ul>
        <li v-for="person in persons" :key='person.id' v-on:click='passData(person)'>
          <p>{{ person.name }}</p>
          
        </li>
      </ul>
      <test-test :my-name="name" :my-message="message"></test-test>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import TestTest from '@/components/TestTest'

export default {
  name: 'HomeView',
  components: {
    // HelloWorld,
    TestTest,
  },
  data() {
    return {
      name: null,
      message: null,
      persons: [
        {
          id: 1,
          name: 'Agaba',
          message: 'kindly pay me'
        },
        {
          id: 2,
          name: 'Frusher',
          message: 'where are you'
        },
        {
          id: 3,
          name: 'Susan',
          message: 'Thanks again'
        },
      ]
    }
  },
  methods: {
    passData(person){
      this.name = person.name
      this.message = person.message
    }
  }
}
</script>
