<script>
  import * as Highcharts from "highcharts";
  import "highcharts/modules/exporting";
  import { Chart } from "@highcharts/svelte";
  import Scroller from "../lib/Scroller.svelte";
  import ArticleTextCloser from "../lib/ArticleTextCloser.svelte";

  let options = {
    chart: {
      type: "bar",
      height: 2100,
      backgroundColor: "#E6E6E6",
      style: {
        fontFamily: "DM Sans",
      },
    },
    title: {
      text: "Median Income by County",
      style: {
        fontFamily: "DM Serif Display",
        fontSize: "1.8em",
      },
    },
    subtitle: {
      text:
        "Source: <a " +
        'href="https://blackwealthdata.org/explore/employment"' +
        'target="_blank">Black Wealth Data Center</a>',
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
      title: {
        text: null,
      },
      gridLineWidth: 1,
      lineWidth: 0,
    },
    yAxis: {
      min: 0,
      title: {
        text: "Dollars",
        align: "high",
      },
      labels: {
        overflow: "justify",
      },
      gridLineWidth: 0,
    },
    tooltip: {
      valuePrefix: "$",
    },
    plotOptions: {
      bar: {
        borderRadius: "50%",
        dataLabels: {
          enabled: true,
        },
        groupPadding: 0.1,
      },
    },
    legend: {
      layout: "vertical",
      align: "right",
      verticalAlign: "top",
      x: -10,
      y: 80,
      width: 155,
      floating: true,
      borderWidth: 1,
      backgroundColor: "var(--highcharts-background-color, #f0f0f0)",
    },
    credits: {
      enabled: false,
    },
    series: [
      {
        name: "Median Income",
        data: [
          34371, 29434, 31495, 36207, 38402, 32976, 45951, 50741, 36259, 35160,
          33188, 38814, 35741, 40265, 49966, 40117, 32131, 33182, 37981, 36723,
        ],
        color: "#0072B2",
      },
      {
        name: "Black Median Income",
        data: [
          33155, 26469, 26201, 29556, 36078, 26812, 40838, 49454, 29779, 26819,
          27799, 29258, 30304, 31902, 43863, 30353, 26250, 27849, 31346, 30149,
        ],
        color: "#5DA899",
      },
    ],
  };

</script>

<div>
  <Scroller layout="left">
    {#snippet sticky()}
      <div class="text">
        <ArticleTextCloser>
          All 20 counties fell into the lower quartile of county median incomes
          in 2023.
        </ArticleTextCloser>

        <ArticleTextCloser>
          Additionally, within each of these counties, the Black median income was less
          than the median income of the county as a whole.
        </ArticleTextCloser>
      </div>
    {/snippet}

    {#snippet scrolly()}
      <div class="chart">
        <Chart {options} highcharts={Highcharts} />
      </div>
    {/snippet}
  </Scroller>
</div>

<style>
  .chart {
    width: 90%;
    margin: 0px auto;
    padding-top: 30px;
    padding-bottom: 30px;
  }

  div {
    background-color: #e6e6e6;
  }

  .text {
    padding-top: 25vh;
    padding-bottom: 20vh;
  }
</style>
