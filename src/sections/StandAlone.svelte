<script>
  import * as Highcharts from "highcharts";
  import "highcharts/modules/exporting";
  import { Chart } from "@highcharts/svelte";
  import ArticleText from "../lib/ArticleText.svelte";
  import Footnote from "../lib/Footnote.svelte";

  const title = "The wealth gap is widely known, ";
  const title2 = "but what health implications could it come with?";
  const subtitle =
    "A closer look at the health disparities in Black communities";
</script>

<div>
  <section>
    <article>
      <ArticleText>
        The impact of a lower income does not end at financial struggles. Having
        a lower income may possibly be linked to greater health risks.
      </ArticleText>
    </article>
    <Footnote>
      Liu, Lili et al. “Impacts of Poverty and Lifestyles on Mortality: A Cohort
      Study in Predominantly Low-Income Americans.” American journal of
      preventive medicine vol. 67,1 (2024): 15-23.
      doi:10.1016/j.amepre.2024.02.015
    </Footnote>
  </section>
</div>

<style>
  div {
    background-color: #e6e6e6;
    display: flex;
    flex-direction: column;
    text-align: center;
  }
  section {
    display: flex;
    height: 100vh;
    justify-content: center;
    flex-direction: column;
    align-items: center;
  }
  article {
    
  }
</style>
