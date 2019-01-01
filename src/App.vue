<template>
  <div id="app">
    <kendo-chart
      :title="title"
      :legend="legend"
      :tooltip="tooltip"
      :series="series"
      :theme="'material'">
    </kendo-chart>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
     title: {
      text: 'Gross Profit'
     },
     legend: {
      position: 'top'
     },
     tooltip: {
      visible: true,
      format: '${0:N}',
      
     },
     series: [{
      type: 'pie',
      data: [{
        category: 'Apple',
        value: 101839000000
      },{
        category: 'Amazon',
        value: 65932000000
      },{
        category: 'IBM',
        value: 36227000000
      },{
        category: 'Microsoft',
        value: 72007000000
      }],
      labels: {
        visible: true,
        template: '#: category #'
      }
     }]
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  margin-top: 60px;
}
</style>
