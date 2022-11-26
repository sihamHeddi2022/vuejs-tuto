<template>
  <div class="hello">
      <p>{{count}}</p>
      <button @click="count++">
        increase
      </button>  
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  methods:{
   
  },
  watch:{
    count(){
      alert("hi there you change the count")
    }
  },
  data(){
    return {
      count:0
     
      
     
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
