<script>
  import * as Highcharts from "highcharts";
  import "highcharts/modules/exporting";
  import { Chart } from "@highcharts/svelte";
  import Scroller from "../lib/Scroller.svelte";
  import ArticleText from "../lib/ArticleText.svelte";

  let options = {
    chart: {
        type: 'bar'
    },
    title: {
        text: 'Undergrad Enrollment Rates by Race/Ethnicity'
    },
    subtitle: {
        text: 'Source: <a ' +
            'href="https://en.wikipedia.org/wiki/List_of_continents_and_continental_subregions_by_population"' +
            'target="_blank">Wikipedia.org</a>'
    },
    xAxis: {
        categories: ['Asian', 'Black', 'Hispanic', 'White'],
        title: {
            text: null
        },
        gridLineWidth: 1,
        lineWidth: 0
    },
    yAxis: {
        min: 0,
        title: {
            text: 'Percentage',
            align: 'high'
        },
        labels: {
            overflow: 'justify'
        },
        gridLineWidth: 0
    },
    tooltip: {
        valueSuffix: ' millions'
    },
    plotOptions: {
        bar: {
            borderRadius: '50%',
            dataLabels: {
                enabled: true
            },
            groupPadding: 0.1
        }
    },
    legend: {
        layout: 'vertical',
        align: 'right',
        verticalAlign: 'top',
        x: -40,
        y: 265,
        floating: true,
        borderWidth: 1,
        backgroundColor: 'var(--highcharts-background-color, #ffffff)',
        shadow: true
    },
    credits: {
        enabled: false
    },
    series: [{
        name: 'Year 2021',
        data: [7.3, 6.4, 6.2, 5.1]
    }, {
        name: 'Year 2023',
        data: [6.9, 5.1, 5.9, 4.8]
    }]
  };
</script>

<div>
  <Scroller layout="left">
    {#snippet sticky()}
      <img
        src="https://images.unsplash.com/vector-1738590593450-647695dbf9d0?q=80&w=880&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
        alt="coding illustration"
      />
      <div class="chart">
        <Chart {options} highcharts={Highcharts} />
      </div>
    {/snippet}

    {#snippet scrolly()}
      <ArticleText>Here is an additional piece of text!</ArticleText>

      <ArticleText>This is another piece of text.</ArticleText>

      <ArticleText>My final piece of text is here.</ArticleText>
    {/snippet}
  </Scroller>
</div>
