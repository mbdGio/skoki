<template>
  <div class="small">
    <line-chart :chart-data="datacollection"></line-chart>
  </div>
</template>

<script>
  import LineChart from './LineChart.js'

  export default {
    components: {
      LineChart
    },
    data () {
      return {
        datacollection: null
      }
    },
    mounted () {
      this.fillData()
    },
    methods: {
      fillData () {
        this.datacollection = {
          labels: [111, 222], //time
          datasets: [
            {
              label: 'X',
              backgroundColor: '#a79aff',
              data: [this.getRandomInt(), this.getRandomInt()]
            }, {
              label: 'Y',
              backgroundColor: '#bffcc6',
              data: [this.getRandomInt(), this.getRandomInt()]
            }, {
              label: 'Z',
              backgroundColor: '#ffabab',
              data: [this.getRandomInt(), this.getRandomInt()]
            }
          ]
        }
      },
      getRandomInt () {
        return Math.floor(Math.random() * (50 - 5 + 1)) + 5
      }
    }
  }
</script>

<style>
  .small {
    max-width: 600px;
    margin:  150px auto;
  }
</style>
