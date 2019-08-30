<template>
<div id="wrapper">
<p>Press the button to initiate the DOM-manipulation tests</p>
<b-form-input id="rowinput" v-model="rows" placeholder="Enter amount of rows"></b-form-input>
<b-button variant="danger" v-if="renderRows" @click="startTest">Toggle</b-button>
<b-button variant="success" v-if="!renderRows" @click="startTest">Toggle</b-button>
<p>Render: {{this.renderRows}}</p>
  <ul v-if="renderRows">
    <li v-for="index in Number(rows)" :key="index">
      {{index}}
    </li>
  </ul>
</div>
</template>

<script>
export default {
  name: "DOM-test",
  props: {
  },
  data(){
    return {
      rows: 10,
      renderRows: false,
    }
  },
  methods: {
    startTest(){
      this.renderRows = !this.renderRows;
    },
  },
  computed:{
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  #result{
    width: 35%;
  }
  #rowinput{
    width: 20%;
    text-align: center;
    margin-left: 40%;
    margin-bottom: 1%;
  }
</style>
