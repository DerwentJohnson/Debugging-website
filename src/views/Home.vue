<template>
  <div class="home">
    <b-table striped hover :items="items"></b-table>
  </div>
</template>

<script>
// @ is an alias to /src


export default {
  name: "home",
  components: {
  },
  data(){
    return {
      items: [
        { Title:'test bug', description:'something', priority:'high', status:'pending' }
      ]
    }
  }
};
</script>
