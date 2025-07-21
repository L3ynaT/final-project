<script>
  import "highcharts/modules/exporting";
  import { onMount } from "svelte";
  import L from "leaflet";

  let map;
  let marker;

  onMount(() => {
    var map = L.map("map").setView([33.878966, -83.400032], 6);

    L.tileLayer(
      "https://{s}.basemaps.cartocdn.com/rastertiles/voyager/{z}/{x}/{y}{r}.png",
      {
        attribution: `&copy;<a href="https://www.openstreetmap.org/copyright" target="_blank">OpenStreetMap</a>,
	        &copy;<a href="https://carto.com/attributions" target="_blank">CARTO</a>`,
        maxZoom: 14,
      }
    ).addTo(map);

    var marker = L.marker([31.961248, -90.982161]).addTo(map);
    marker.bindPopup("<b>Claiborne County, MS</b><br>86.2%").openPopup();

    var marker = L.marker([33.114072, -90.053049]).addTo(map);
    marker.bindPopup("<b>Holmes County, MS</b><br>82.4%").openPopup();

    var marker = L.marker([32.841031, -87.887813]).addTo(map);
    marker.bindPopup("<b>Greene County, AL</b><br>81.5%").openPopup();

    var marker = L.marker([31.711173, -91.06034]).addTo(map);
    marker.bindPopup("<b>Jefferson County, MS</b><br>81.2%").openPopup();

    var marker = L.marker([34.686492, -90.383476]).addTo(map);
    marker.bindPopup("<b>Tunica County, MS</b><br>79.6%").openPopup();

    var marker = L.marker([33.183698, -90.489321]).addTo(map);
    marker.bindPopup("<b>Humphreys County, MS</b><br>78.8%").openPopup();

    var marker = L.marker([32.431028, -85.707801]).addTo(map);
    marker.bindPopup("<b>Macon County, AL</b><br>78.3%").openPopup();

    var marker = L.marker([37.227618, -77.394928]).addTo(map);
    marker.bindPopup("<b>Petersburg city, VA</b><br>77.2%").openPopup();

    var marker = L.marker([34.200812, -90.571414]).addTo(map);
    marker.bindPopup("<b>Coahoma County, MS</b><br>75.9%").openPopup();

    var marker = L.marker([32.183521, -86.580704]).addTo(map);
    marker.bindPopup("<b>Lowndes County, AL</b><br>74.5%").openPopup();

    var marker = L.marker([33.516672, -90.180385]).addTo(map);
    marker.bindPopup("<b>Leflore County, MS</b><br>74.5%").openPopup();

    var marker = L.marker([33.105964, -88.560918]).addTo(map);
    marker.bindPopup("<b>Noxubee County, MS</b><br>73.8%").openPopup();

    var marker = L.marker([32.905941, -90.877673]).addTo(map);
    marker.bindPopup("<b>Sharkey County, MS</b><br>73.7%").openPopup();

    var marker = L.marker([33.451461, -90.655584]).addTo(map);
    marker.bindPopup("<b>Sunflower County, MS</b><br>73.0%").openPopup();

    var marker = L.marker([32.297093, -90.180801]).addTo(map);
    marker.bindPopup("<b>Hinds County, MS</b><br>72.4%").openPopup();

    var marker = L.marker([33.397767, -91.037962]).addTo(map);
    marker.bindPopup("<b>Washington County, MS</b><br>72.2%").openPopup();

    var marker = L.marker([34.256528, -90.273232]).addTo(map);
    marker.bindPopup("<b>Quitman County, MS</b><br>72.2%").openPopup();

    var marker = L.marker([33.275346, -82.976309]).addTo(map);
    marker.bindPopup("<b>Hancock County, GA</b><br>71.4%").openPopup();

    var marker = L.marker([32.583884, -88.18684]).addTo(map);
    marker.bindPopup("<b>Sumter County, AL</b><br>71.2%").openPopup();

    var marker = L.marker([32.143306, -85.715404]).addTo(map);
    marker.bindPopup("<b>Bullock County, AL</b><br>71.2%").openPopup();
  });
</script>

<div>
  <section>
    <h1>
      A dive into the <a href="https://blackwealthdata.org/explore/population">20 U.S. counties</a> with the highest Black population
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
  a {
    color: black;
  }
  #map {
    background-color: #ffffff;
    height: 110vh;
  }
  @import "leaflet/dist/leaflet.css";
</style>
