<template>
  <div id="child">
    <h2>i'm child</h2>
    <p>someData: {{someData}}</p>
    <p class="colorful">flowData: {{flowData}}</p>
    <button v-on:click="changeFatherData">click it!</button>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        changeSomeData: 'If you see this, means .sync could transmit two-way flowdata'
      }
    },
    props: [
      'someData',
      'flowData'
    ],
    methods: {
      changeFatherData: function () {
        this.$emit('update:someData', this.changeSomeData);
      }
    }
  }
</script>
<style>

  #child {
    border: 1px solid yellowgreen;
  }

</style>
