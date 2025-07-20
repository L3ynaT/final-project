<script>
  import * as Highcharts from "highcharts";
  import "highcharts/modules/exporting";
  import { Chart } from "@highcharts/svelte";
  import { onMount } from "svelte";
  import L from "leaflet";

  let map;
  let marker;

  onMount(() => {
    var map = L.map("map").setView([33, -82], 6);

    L.tileLayer('https://{s}.basemaps.cartocdn.com/rastertiles/voyager/{z}/{x}/{y}{r}.png',
	    {
	      attribution: `&copy;<a href="https://www.openstreetmap.org/copyright" target="_blank">OpenStreetMap</a>,
	        &copy;<a href="https://carto.com/attributions" target="_blank">CARTO</a>`,
	      subdomains: 'abcd',
	      maxZoom: 14,
	    }).addTo(map);

    var marker = L.marker([33.275346, -82.976309]).addTo(map);
    marker.bindPopup("<b>Hancock County, GA</b><br>I am a popup.").openPopup();

    
  });
</script>

<div>
  <section>
    <h1>
      A dive into the 20 U.S. counties with the highest Black population
      percentage
    </h1>
  </section>
  <section id="map"></section>
</div>

<style>
  div {
    display: flex;
  }
  section {
    display: flex;
    height: 110vh;
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
  #map {
    background-color: #ffffff;
    height: 110vh;
  }
  @import "leaflet/dist/leaflet.css";
</style>
