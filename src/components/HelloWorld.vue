
<template>
  <div>
    <div id="mapContainer"
         style="width:100%;height:500px">
    </div>
  </div>

</template>

<script>
import AMap from 'AMap'
// import AMapUI from 'AMapUI'

export default {
  mounted () {
    this.amapView()
  },
  methods: {
    amapView () {
      const map = new AMap.Map('mapContainer', {
        zoom: 11,
        center: [116.397428, 39.90923],
        viewMode: '3D'
      })
      map.plugin(['AMap.ToolBar', 'AMap.MapType'], function () {
        map.addControl(new AMap.ToolBar())
        map.addControl(new AMap.MapType({ showTraffic: false, showRoad: false }))
      })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
