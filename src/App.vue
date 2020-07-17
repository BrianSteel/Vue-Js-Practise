<template>
  <div>
    <h1>{{title}}</h1>
    <header-ninja :title="title3" @changeTitle="updateTitle($event)"></header-ninja>

    <ninja-body :ninjas="ninjas"></ninja-body>
    <hr />
    <ninja-body :ninjas="ninjas"></ninja-body>
    <hr />
    <ninja-body :ninjas="ninjas2"></ninja-body>
     <hr />
    <ninja-body :ninjas="ninjas2"></ninja-body>
    <footer-ninja :title="title3"></footer-ninja>
  </div>
</template>

<script>
import Header from "./component/Header.vue";
import Footer from "./component/Footer.vue";
import Ninja from "./component/Ninja.vue";
export default {
  //components
  components: {
    "header-ninja": Header,
    "footer-ninja": Footer,
    "ninja-body": Ninja
  },
  data() {
    return {
      title: "First Vue File",
      ninjas: [
        { name: "Vegeta", specialty: "Galek gun", show: false },
        { name: "Goku", specialty: "Instant transmision", show: false },
        { name: "Gohan", specialty: "Super Kamehameha", show: false },
        { name: "Picolo", specialty: "Special cannon beam", show: false },
        { name: "Beerus", specialty: "Godly wipe", show: false },
        { name: "Broly", specialty: "Legendary super saiyan", show: false },
        { name: "Freeza", specialty: "Golden Freeza", show: false },
        { name: "Cell", specialty: "Copy Techniques", show: false },
        { name: "Buu", specialty: "Regenerate", show: false }
      ],
      ninjas2: [
        { name: "Freeza", specialty: "Golden Freeza", show: false },
        { name: "Cell", specialty: "Copy Techniques", show: false },
        { name: "Buu", specialty: "Regenerate", show: false }
      ],
      title3: "New new Footer"
    };
  },
  methods: {
    updateTitle: function(updateTitle){
      this.title3=updateTitle;
    }
  }
};
</script>
<style>
html{
  padding: 0;
  margin: 0;
}
body{
  background: #eee;
}
</style>

<style scoped>
html{
  padding: 0;
  margin: 0;
}
body{
  background: #999;
}
h1 {
text-align: center;
  color: purple;
}
</style>
