<template>
  <div>
    <svg viewbox="0 0 900 600" class="chart" preserveAspectRatio="xMaxYMax meet">
      <!-- <polyline fill="none" stroke="#0074d9" stroke-width="2" :points="performance"/> -->
      <!-- x-axis -->
      <line stroke="#333333" x1="50" y1="200" x2="300" y2="200"></line>
      <g class="x-labels">
        <text x="400" y="250">Hour</text>
        <text x="50" y="220">8am</text>
        <text x="100" y="220">9am</text>
        <text x="150" y="220">10am</text>
        <text x="200" y="220">11am</text>
        <text x="250" y="220">12pm</text>
        <text x="300" y="220">1pm</text>
        <text x="350" y="220">2pm</text>
        <text x="400" y="220">3pm</text>
        <text x="450" y="220">4pm</text>
        <text x="500" y="220">5pm</text>
        <text x="550" y="220">6pm</text>
        <text x="600" y="220">7pm</text>
        <text x="650" y="220">8pm</text>
        <text x="700" y="220">9pm</text>
        <text x="750" y="220">10pm</text>
      </g>
      <!-- y-axis -->
      <line stroke="#333333" x1="50" y1="0" x2="50" y2="200"></line>
      <g class="y-labels">
        <text x="20" y="170" transform="rotate(-90, 10, 170)">Performance</text>
        <text x="30" y="220">0</text>
        <text x="30" y="200">20</text>
        <text x="30" y="180">40</text>
        <text x="30" y="160">60</text>
        <text x="30" y="140">80</text>
        <text x="30" y="120">100</text>
      </g>
      <polyline
        fill="#218649"
        stroke="#0074d9"
        stroke-width="2"
        :points="performance"
      />
    </svg>
  </div>
</template>

<script>
export default {
  name: "SvgLineChart",
  // TODO - I can create a data object with hour and performance and then in a method loop over the object and pull the points as an array of [x,y] coordinates
  data: () => ({
    // subtract start time so if 8am subtract 8 from x and then multiply by 50
    // y coordinate is height minus actual statistic
    performance: [[50,200],[100,145],[150,115],[200,125],[250,140],[300,155],[350,175],[400,185],[450,170],[500,160],[550,155],[600,145],[650,145],[700,155],[750,200]],
    performanceTest:"8,0 9,55 10,85 11,75 12,60 13,45 14,25 15,15 16,30 17,40 18,45 19,55 20,55 21,45 22,0"
  })
}
</script>

<style scoped>

body {
  /* background: #ccc; */
  display: flex;
  align-items: center;
  justify-content: center;
}

body, html {
  height: 100%;
}
.x-labels,
.y-labels {
  fill: black;
  text-anchor: middle;
  font-size: 12px;
  text-emphasis: 800;
}
.chart {
  background: white;
  margin: 0 auto;
  text-align: center;
  width: 1000px;
  height: 300px;
}
</style>