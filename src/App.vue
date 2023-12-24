<script setup> /**Composition API */
import {ref} from "vue";
  const count = ref(0);

  const addToCount = () => {
    console.log("ADDING")
    count.value = count.value + 1
  }

  const minusFromCount = () => {
    console.log("MINUS")
    count.value = count.value - 1
  }
</script>

<!-- <script> /**Option API */
  export default{
    data(){
      return{
        count: 0
      }
    },
    methods: {
      addToCount(){
        this.count = this.count + 1
      },
      minusFromCount(){
        this.count = this.count - 1
      }
    }
  }
</script> -->

<template>
  <main>
    <div>
    <h4>
      The current count is...
    </h4>
    <h1>{{ count }}</h1>
    <button @click="minusFromCount">-</button>
    <button @click="addToCount">+</button>
  </div>
  </main>
</template>

<style scoped> /**scope here means that it will be in this scope of file**/
  main{
    background-color: grey;
    height: 100vh;
    width: 100vw;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  div{
    text-align: center;
  }
</style>