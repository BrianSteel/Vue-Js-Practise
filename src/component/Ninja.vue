
<template>
  <div id="ninjas">
    <ul>
      <li v-for="ninja in ninjas" v-bind:key="ninja.name" @click="ninja.show = !ninja.show">
        <h2>{{ninja.name}}</h2>
        <h3 v-show="ninja.show">{{ninja.specialty}}</h3>
      </li>
<!--       <li v-for="ninja2 in ninjas2" v-bind:key="ninja2.name" @click="ninja2.show = !ninja2.show">
        <h2>{{ninja2.name}}</h2>
        <h3 v-show="ninja2.show">{{ninja2.specialty}}</h3>
      </li> -->
    </ul>
    <button @click="deleteNinja">Delete Ninja</button>
  </div>
</template>

<script>
export default {
  props: {
    ninjas: {
      type: Array,
      required: true
    }/* ,
    ninjas2: {
      type: Array,
      required: true
    } */
  },
  data() {
    return {};
  },
  methods: {
      deleteNinja: function(){
          this.ninjas.pop();
 /*          this.ninjas2.pop(); */
      }
  },
  computed: {}
};
</script>


<style scoped>
#ninjas {
  width: 100%;
  max-width: 1200px;
  margin: 40px auto;
  padding: 0 20px;
  box-sizing: border-box;
}

ul {
  display: flex;
  flex-wrap: wrap;
  list-style-type: none;
  padding: 0;
}

li {
  flex-grow: 1;
  flex-basis: 300px;
  text-align: center;
  padding: 30px;
  border: 1px solid #222;
  margin: 10px;
}
</style>