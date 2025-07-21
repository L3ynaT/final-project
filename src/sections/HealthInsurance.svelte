<script>
  import "highcharts/modules/exporting";
  import ArticleText from "../lib/ArticleText.svelte";
  import Scroller from "../lib/Scroller.svelte";
  import * as Highcharts from "highcharts";
  import { Chart } from "@highcharts/svelte";

  let options = {
    chart: {
      type: "column",
      height: "700",
      backgroundColor: "#E6E6E6",
      style: {
        fontFamily: "DM Sans",
      },
    },
    title: {
      text: "Health Insurance Coverage (2023)",
      style: {
        fontFamily: "DM Serif Display",
        fontSize: "1.8em",
      },
    },
    subtitle: {
      text:
        'Source: <a target="_blank" ' +
        'href="https://blackwealthdata.org/explore/employment">Black Wealth Data Center</a>',
      style: {
        textDecorationLine: "underline",
      },
    },
    xAxis: {
      categories: [
        "Claiborne County, MS",
        "Holmes County, MS",
        "Greene County, AL",
        "Jefferson County, MS",
        "Tunica County, MS",
        "Humphreys County, MS",
        "Macon County, AL",
        "Petersburg city, VA",
        "Coahoma County, MS",
        "Lowndes County, AL",
        "Leflore County, MS",
        "Noxubee County, MS",
        "Sharkey County, MS",
        "Sunflower County, MS",
        "Hinds County, MS",
        "Washington County, MS",
        "Quitman County, MS",
        "Hancock County, GA",
        "Sumter County, AL",
        "Bullock County, AL",
      ],
      crosshair: true,
      accessibility: {
        description: "Counties",
      },
    },
    yAxis: {
      min: 0,
      title: {
        text: "Total Population Percentage with Health Insurance",
      },
    },
    tooltip: {
      valueSuffix: "%",
    },
    plotOptions: {
      column: {
        pointPadding: 0.1,
        borderWidth: 0,
      },
    },
    series: [
      {
        name: "Percentage",
        data: [
          81.9, 89.4, 86.2, 91.3, 86.9, 85.6, 90.9, 91.8, 86.8, 91.5, 85.9,
          80.0, 85.8, 88.6, 87.2, 87.8, 87.2, 92.0, 90.8, 87.1,
        ],
        color: "#0072B2",
      },
    ],
  };
</script>

<div>
  <Scroller layout="right">
    {#snippet sticky()}
      <div class="chart">
        <Chart {options} highcharts={Highcharts} />
      </div>
    {/snippet}

    {#snippet scrolly()}
      <div class="text">
        <ArticleText>
          In 2023, 12 of the 20 counties fell into the lower quartile of health
          insurance coverage percentage. The remaining 8 counties were in the
          second quartile.
        </ArticleText>
        <ArticleText>
          All 20 counties were in the bottom two quartiles, meaning they were
          all below the median total population percentage with health
          insurance.
        </ArticleText>
      </div>
    {/snippet}
  </Scroller>
</div>

<style>
  .text {
    padding-bottom: 300px;
    background-image: linear-gradient(
      to right,
      rgba(255, 0, 0, 0),
      rgba(148, 203, 236, 1)
    );
  }
  .chart {
    width: 90%;
    padding-top: 17vh;
    padding-bottom: 28vh;
  }
</style>
