<template>
  <div class="hello">
     <p>
        skkskskskskskskskks
     </p>
     
     <!-- Event modifier -->

     <button type="submit" @click.prevent="($event)=>submit($event)">
        submit
     </button>

     {{ok2}}
   
    <input type="text" :value="count" @keyup.enter="count++">
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  methods:{
    submit(e){
      console.log(e);
      this.ok2 = true
    }
  },
  data(){
    return {
      count:0,
      ok1:true,
      ok2:false,
      
     
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
