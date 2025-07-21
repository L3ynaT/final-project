<script>
  import * as Highcharts from "highcharts";
  import "highcharts/modules/exporting";
  import { Chart } from "@highcharts/svelte";
  import ScrollerBlueVer from "../lib/ScrollerBlueVer.svelte";
  import ArticleText from "../lib/ArticleText.svelte";

  let options = {
    chart: {
      type: "pie",
      backgroundColor: "#94CBEC",
      height: 600,
      style: {
        fontFamily: "DM Sans",
      },
    },
    title: {
      text: "",
      style: {
        fontFamily: "DM Serif Display",
      },
    },
    plotOptions: {
      pie: {
        borderColor: "#94CBEC",
        allowPointSelect: true,
        dataLabels: [
          {
            enabled: true,
            distance: 20,
          },
          {
            enabled: true,
            distance: -50,
            format: "{point.percentage:.1f}%",
            style: {
              fontSize: "1.4em",
              textOutline: "none",
            },
            filter: {
              operator: ">",
              property: "percentage",
              value: 10,
            },
          },
        ],
      },
    },
    series: [
      {
        name: "Number of Counties",
        data: [
          {
            name: "Severe Shortage",
            selected: true,
            y: 11,
            color: "#E6E6E6",
          },
          {
            name: "Moderate Shortage",
            y: 1,
            color: "#5DA899",
          },
          {
            name: "No Designated Shortage",
            y: 8,
            color: "#0072B2",
          },
        ],
      },
    ],
  };
</script>

<div>
  <ScrollerBlueVer layout="left">
    {#snippet sticky()}
      <div class="chart">
        <Chart {options} highcharts={Highcharts} />
      </div>
    {/snippet}

    {#snippet scrolly()}
      <div class="text">
        <ArticleText>
          12 of the 20 counties were considered a primary care <a
            href="https://blackwealthdata.org/explore/employment"
            >health professional shortage area</a
          > (HPSA) in 2024. The higher the primary care HPSA score, the more severe
          the shortage.
        </ArticleText>

        <ArticleText>
          1 of those 12 counties had a moderate shortage (primary care HPSA
          score: 1-15)
        </ArticleText>

        <ArticleText>
          The remaining 11 counties had a severe shortage (primary care HPSA
          score: 16-25)
        </ArticleText>
      </div>
    {/snippet}
  </ScrollerBlueVer>
</div>

<style>
  .chart {
    width: 90%;
    margin: 0px auto;
    padding-top: 200px;
    padding-bottom: 200px;
  }

  .text {
    padding-bottom: 200px;
  }

  a {
    color: #0072b2;
  }
</style>
