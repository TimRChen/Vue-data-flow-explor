<template>
  <div id="foo">
    <h1>case-1:</h1>
    <h3>.sync 双向数据流的探究，是否应该使用其作为子组件向父组件通信的方法</h3>
    <div class="case-1">
      <h1>father</h1>
      <h2>someData: {{someData}}</h2>
      <child-data v-bind:someData.sync="someData" v-bind:flowData="flowData"></child-data>
    </div>

    <h1>case-2</h1>
    <h3>v-model子向父传递数据方式差异探索</h3>
    <div class="case-2">
      <h1>father</h1>
      <div class="colorful">modelData: {{modelData}}</div>
       <input type="text" v-model="modelData"> 
      <child-data-1 v-model="modelData"></child-data-1>
    </div>

  </div>
</template>
<script>
  import childData from './childData';
  import childData1 from './childData1';

  export default {
    data() {
      return {
        // case-1
        someData: 'this is a msg by father',
        flowData: 'this is flowData by father',

        // case-2
        modelData: 'init data by father',
      }
    },
    components: {
      childData,
      childData1
    },
    methods: {

    }
  }
</script>
<style>

  .case-1 {
    margin-bottom: 30px;
    padding: 10px;
    border: 1px solid burlywood;    
  }


  .case-2 {
    margin-bottom: 30px;
    padding: 10px;
    border: 1px solid black;    
  }

  #foo {
    width: 400px;
  }

  .colorful {
    color: darkcyan;
  }


</style>
