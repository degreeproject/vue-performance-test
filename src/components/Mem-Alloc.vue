<template>
<div id="wrapper">
<p>Press the buttons to initiate the memory allocation test tests</p>
<b-form-input id="arraySizeInput" v-model="arraySize" placeholder="Enter array size"></b-form-input>
<b-button variant="primary" @click="randomArray(arraySize, 1, 100)">Generate array</b-button>
<b-button variant="success" @click="startTest">Run test</b-button>
<b-button variant="danger" @click="clearArrays">Reset all</b-button>
  <ul id="oldArray">
    <li v-for="index in oldArray" :key="index">
      {{index}}
    </li>
  </ul>
  <ul id="newArray">
    <li v-for="index in newArray" :key="index">
      {{index}}
    </li>
  </ul>
</div>
</template>

<script>
export default {
  name: "Mem-Alloc",
  props: {
  },
  data(){
    return {
      oldArray: [],
      newArray: [],
      arraySize: 1
    }
  },
  methods: {
    startTest(){
      this.newArray = this.oldArray;
    },
    clearArrays(){
      this.oldArray = [],
      this.newArray = []
    },
    randomArray(size) {
    let i = 0
     this.oldArray = Array.from({length: size}, () => i++);
    }
  },
  computed:{
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  #oldArray{
    position: absolute;
    width: 30%;
    left: 0;
  }
  #newArray{
    position: absolute;
    width: 30%;
    right: 0;
  }
  #arraySizeInput{
    width: 20%;
    text-align: center;
    margin-left: 40%;
    margin-bottom: 1%;
  }
</style>
