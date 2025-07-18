<script>
  import * as Highcharts from "highcharts";
  import "highcharts/modules/exporting";
  import { Chart } from "@highcharts/svelte";

  const title = "The wealth gap is widely known, ";
  const title2 = "but what health implications could it come with?";
  const subtitle =
    "A closer look at the health disparities in Black communities";
</script>

<div>
  <section>
    <h1>
      A dive into the 20 U.S. counties with the highest Black population
      percentage
    </h1>
  </section>
  <section class="map"></section>
</div>

<style>
  div {
    display: flex;
  }
  section {
    display: flex;
    height: 100vh;
    align-items: center;
    float: left;
    width: 50%;
    background-color: #94cbec;
  }
  h1 {
    margin: 0;
    font-family: "DM Serif Display";
    text-align: right;
    font-size: 3rem;
    padding: 70px;
  }
  .map {
    background-color: #ffffff;
  }
</style>
