<template>
  <div id="child">
    <h2>i'm child</h2>
    <div class="colorful">modelData: {{modelData}}</div>
    <p>child中modelData无值则表示父组件不能通过v-model将值传入子组件</p>
    <button v-on:click="changeInput">change input value</button> 
  </div>
</template>
<script>
  export default {
    data() {
      return {
        changeWord: 'this changeData by child'
      }
    },
    props: ['modelData'],
    methods: {
      changeInput: function () {
        this.$emit('input', this.changeWord);
      }
    },
  }
</script>
<style>

  #child {
    border: 1px solid black;
    padding-bottom: 30px;
  }

</style>
