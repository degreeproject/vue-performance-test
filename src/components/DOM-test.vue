<template>
<div id="wrapper">
<p>Press the button to initiate the DOM-manipulation tests</p>
<b-form-input id="rowinput" v-model="arraySize" placeholder="Enter amount of rows"></b-form-input>
<b-button variant="primary" @click="randomArray(arraySize)">Prepare array</b-button>
<b-button variant="success" @click="startTest">Render</b-button>
<b-button variant="danger" @click="clearArray">Clear</b-button>
<b-button variant="warning" @click="changeArray">Change</b-button>
<p>Set array size: {{array.length}}</p>
<p>Rendering: {{renderRows}}</p>
  <ul v-if="renderRows">
    <li v-for="index in array" :key="index">
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
      array: [],
      arraySize: 1,
      renderRows: false,

    }
  },
  methods: {
    startTest(){
      this.renderRows = !this.renderRows;
    },
    changeArray(){
      this.array = this.array.map(e => e + 1)
    },
    clearArray(){
      this.array = []
    },
    randomArray(size) {
      let i = 0
      this.array = Array.from({length: size}, () => i++);
    }
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
