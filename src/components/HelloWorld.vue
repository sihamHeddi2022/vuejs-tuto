<template>
  <div class="hello">
   
     <p v-for="item in array1" :key="item.id">
         {{item}}
     </p>
       <p v-for="item in arrayObject" :key="item.id">
         {{item.name}}
       </p>
      <hr>
        <p v-for="({name},index) in arrayObject" :key="index">
         {{name}} -  {{index}} 
       </p>
          <hr>
        <p v-for="n in 10" :key="n.id">
          {{n}}
        </p>
        <h1 v-if="ok2">
              kskkskskskksks
        </h1>
        <p v-else>nothing</p>
        <!-- you can use v-if in template -->
        <p v-for="n in 10" :key="n" >
          <span  v-if="ok1">{{n}}</span>
        </p>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
 
  data(){
    return {
      ok1:true,
      ok2:false,
      array1:["hdhdhd","dhdhdh","jjdjdjdjd"],
      arrayObject:[
        {
         name:"suzan",

        },
        {
         name:"amel"
        }
      ]
     
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
