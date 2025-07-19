<script>
  import "highcharts/modules/exporting";
  import ArticleTextCloser from "../lib/ArticleTextCloser.svelte";
  import Footnote from "../lib/Footnote.svelte";
</script>

<div>
  <section>
    <article>
      <ArticleTextCloser>
        The impact of a lower income does not end at financial struggles. Having
        a lower income may possibly be linked to greater health risks.
      </ArticleTextCloser>
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
    height: 110vh;
    justify-content: center;
    flex-direction: column;
    align-items: center;
  }
</style>
