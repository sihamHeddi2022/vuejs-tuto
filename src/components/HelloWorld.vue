<template>
  <div class="hello">

    {{msg}}
    <div :id="id" v-html='content'></div>
    <a :href="url">google</a>
    {{sum()}}
    {{ ok? "yeah I'm here" : "No . I don't want to meet her. I hate her "}}
    <p v-if="ok">Go out right now and don't back again to my house</p>
    <button @click="submit">submit</button>
    <p>{{concatenate}}</p>
    <span :[attr]="red">hi there</span>
    <p :style="[style,style2]">dsjdsjds sdjdsjdsjdsjjds</p>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  methods:{
    sum(){
      return 1+1
    },

    submit(){
      this.ok = false
    }
  },
  computed:{
    concatenate(){
      return this.attr+"  "+this.id
    }
  },
  data(){
    return {
      id:"ksksk",
      ok:true,
      url:"www.google.com",
      msg :"  hello world !",
      content:"<b>hi there</b>",
      attr :"class",
      red:"red",
      style:{
        fontSize:"18px",
        color:"green"
      },
      style2:{
        textDecoration:"underline"
      }
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.red {
  color:red
}
</style>
