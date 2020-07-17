
<template>
<footer>
    <h1>{{copywrite}} {{title}}</h1>
</footer>
</template>

<script>
//write Footer.vue
//import
//list as component (locally or globally)
//provide tag
import {bus} from '../main.js';
export default {
  props: {
        title: {
            type: String,
            required: true
        },
    },
  data () {
    return {
     copywrite: 'Vue Ninja Footer'
    }
  },
  created(){
    bus.$on("changeTitle", (data)=>{
      this.title = data;
    })
  },
  methods: {
  }
}
</script>


<style scoped>
footer{
    background: rgb(54, 56, 54);;
    padding: 10px;
}
h1{
   color: #ddd;
   text-align: center; 
}

</style>