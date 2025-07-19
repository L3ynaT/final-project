

<div>
  <section>
    <h1>
      A dive into the 20 U.S. counties with the highest Black population
      percentage
    </h1>
  </section>
  <div class="map"></div>
</div>

<script>
  import "highcharts/modules/exporting";
  import { Chart } from "@highcharts/svelte";
  import * as L from "leaflet";
  // If you're playing with this in the Svelte REPL, import the CSS using the
  // syntax in svelte:head instead. For normal development, this is better.
  import "leaflet/dist/leaflet.css";
  var map = L.map("map").setView([51.505, -0.09], 13);
  L.tileLayer("https://tile.openstreetmap.org/{z}/{x}/{y}.png", {
    maxZoom: 19,
    attribution:
      '&copy; <a href="http://www.openstreetmap.org/copyright">OpenStreetMap</a>',
  }).addTo(map);
</script>

<style>
  div {
    display: flex;
  }
  section {
    display: flex;
    height: 110vh;
    align-items: center;
    float: left;
    width: 40%;
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
    height: 110vh;
  }
</style>
