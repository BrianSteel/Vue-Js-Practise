<template>
<header>
    <h1 @click="changeTitle">{{title}}</h1>
</header>
</template>

<script>
import {bus}  from '../main.js';
export default {
    props: {
        title: {
            type: String,
            required: true
        },
    },
  data () {
    return {
     
    }
  },
  methods: {
        changeTitle: function(){
        /* this.title = 'new new header' */
        //I want primitive data to behave like reference data
        //this.$emit('changeTitle', 'New new header')
        this.title = "New new header";// this gives an error that will be fixed later on when you learn.. also this mutates only for header
        bus.$emit('changeTitle', "New new header")// this gives an error that will be fixed later on when you learn.. also this mutates only for footer
    }
  },
}
</script>


<style scoped>
header{
    background: lightgreen;;
    padding: 10px;
}
h1{
   color: #222;
   text-align: center; 
}

</style>
