<template>
<div id="wrapper">
  <div id='result'>
    <b-table striped hover :items="this.data"></b-table>
  </div>
</div>
  
</template>

<script>
export default {
  name: "grid",
  props: {
    data: Array,
    columns: Array,
  },
  data(){
    return {
      searchQuery: '',
      sortKey: '',
      sortOrders: {},
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#result{
  width: 35%;
}
</style>
