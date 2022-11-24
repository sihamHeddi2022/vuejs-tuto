<template>
  <div class="hello">
      <input type="text" :value="salary" @input="salary=$event.target.value">
       <input type="number" v-model.number="counter">
      <br>
      
      <select v-model="levels" multiple>
          
          <option v-for="({name,value},index) in options" :key="index" :value="value" >
            {{name}}
          </option>
          

      </select>
      

      <br>
      
      <input type="checkbox" name="sex" value="man" id="man" v-model="sex">
      <label for="man">man</label>
     
      <br>
     
      <input type="checkbox" name="sex" value="woman" id="woman" v-model="sex">
      <label for="woman">woman</label>
      <br>

      <input type="checkbox" name="sex" value="other"  id="other" v-model="sex">
      <label for="other">other</label>
      <br>
      
<!--       <input type="radio" value="car" id="car" name="vehicule" :checked="car" @change="car = !$event.target.checked">
      <label for="car">car</label>
             
      <input type="radio" value="bus" id="bus"  name="vehicule" :checked="bus"  @change="bus = $event.target.checked">
      <label for="bus">bus</label> -->

  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  methods:{
   
  },
  data(){
    return {

      salary:10000,
      counter:4,
      levels:[],
      sex:[],
      car:false,
      bus:true,
      options:[
        {
          name:"level1",
          value:1
        },
        {
          name:"level2",
          value:2
        },
        {
          name:"level3",
          value:3
        },
        {
          name:"level4",
          value:4
        },
        {
          name:"level5",
          value:5
        }
      ]
    
      
     
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
