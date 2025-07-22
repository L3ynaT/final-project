<script>
  import * as Highcharts from "highcharts";
  import "highcharts/modules/exporting";
  import { Chart } from "@highcharts/svelte";
  import ArticleText from "../lib/ArticleText.svelte";
  import TitleCard from "../lib/TitleCard.svelte";
  import ScrollerStack from "../lib/ScrollerStack.svelte";
  import FullPage from "../lib/FullPage.svelte";
  import Gradient from "../lib/Gradient.svelte";

  const title = "The Intersection of Income and Healthcare";
  const title2 = " in Black Communities";
  const subtitle =
    "The wealth gap is widely known, but what health implications could it come with?";

  let options = {
    chart: {
      height: 570,
      backgroundColor: "#E6E6E6",
      style: {
        fontFamily: "DM Sans",
      },
    },
    title: {
      text: "Median Annual Earnings for Full-Time Workers (25-34 Years Old, All Education Levels, Nationwide) by Race/Ethnicity",
      align: "left",
      style: {
        fontFamily: "DM Serif Display",
        fontSize: "1.8em",
      },
      
    },

    subtitle: {
      text: 'Source: <a href="https://blackwealthdata.org/explore/employment" target="_blank">Black Wealth Data Center</a>.',
      align: "left",
      style: {
        textDecorationLine: "underline",
      },
    },

    yAxis: {
      title: {
        text: "Median Annnual Earnings (dollars)",
      },
    },

    xAxis: {
      title: {
        text: "Year",
      },
      accessibility: {
        rangeDescription: "Range: 2012 to 2022",
      },
    },

    legend: {
      layout: "vertical",
      align: "right",
      verticalAlign: "middle",
    },

    plotOptions: {
      series: {
        label: {
          connectorAllowed: false,
        },
        pointStart: 2012,
      },
    },
    tooltip: {
      valuePrefix: "$",
    },

    series: [
      {
        name: "Hispanic",
        data: [
          39260, 38580, 38880, 39840, 41420, 42090, 42790, 43180, 46310, 45490,
          45610,
        ],
        color: "#ab6ad6",
      },
      {
        name: "White",
        data: [
          53110, 53140, 52580, 56060, 55910, 56040, 57450, 58760, 59790, 59620,
          58120,
        ],
        color: "#0072B2",
      },
      {
        name: "Asian",
        data: [
          67110, 64740, 62910, 64400, 67210, 73300, 71130, 70540, 81160, 78740,
          81030,
        ],
        color: "#5DA899"
      },
      {
        
        name: "Black",
        data: [
          40930, 42810, 39190, 43440, 41980, 42170, 42740, 43660, 46550, 45170,
          46040,
        ],
        color: "#4048b6",
      },
    ],

    responsive: {
      rules: [
        {
          condition: {
            maxWidth: 500,
          },
          chartOptions: {
            legend: {
              layout: "horizontal",
              align: "center",
              verticalAlign: "bottom",
            },
          },
        },
      ],
    },
  };

</script>

<div>
  <ScrollerStack layout="left">
    {#snippet sticky()}
      <TitleCard {title} {title2} {subtitle} />
    {/snippet}

    {#snippet scrolly()}
      <Gradient direction="up"></Gradient>
      <FullPage>
        <div class="content">
          <section class="text">
          <ArticleText
            >In 2022, the median annual earnings for Black full-time workers
            (25-34 years old of all education levels) was $46,040, one of the
            lowest earnings compared to other racial/ethnic groups.</ArticleText
          ></section>
          <div class="chart">
            <Chart {options} highcharts={Highcharts} />
          </div>
        </div>
      </FullPage>
    {/snippet}
  </ScrollerStack>
</div>

<style>
  .content {
    display: flex;
    align-items: center;
  }
  .text {
    margin: 30px;
    padding-bottom: 250px;
  }
  .chart {
    margin-right: 120px;
    width: 100%;
  }
</style>
