<script>
  import "highcharts/modules/exporting";
  import ArticleTextCloser from "../lib/ArticleTextCloser.svelte";
  import ArticleText from "../lib/ArticleText.svelte";
  import TitleCard from "../lib/TitleCard.svelte";
  import ScrollerStack from "../lib/ScrollerStack.svelte";
  import FullPage from "../lib/FullPage.svelte";
  import Gradient from "../lib/Gradient.svelte";
</script>

<div>
  <ArticleText>
    While many <a href="https://www.forbes.com/sites/omerawan/2025/06/04/how-income-can-affect-your-health-and-population-health/">factors</a> may play a role in these findings, such as living
    conditions and stress, this data suggests that having a <a href="https://www.ncbi.nlm.nih.gov/books/NBK578537/">low income</a> can be a
    factor in making access to healthcare more challenging.
  </ArticleText>
  <ArticleText
    >Affording health insurance can be difficult, and, even with health
    insurance, there may be additional barriers to receiving healthcare due to
    the shortage of primary care health professionals in these counties.
  </ArticleText>
  <ArticleText
    >While disparities exist in many areas, this data highlights that Black
    communities may be more disproportionately impacted.
  </ArticleText>
</div>

<style>
  div {
    background-image: linear-gradient(rgba(148,203,236,1), rgba(148,203,236,0.3));
    padding-top: 10px;
    padding-bottom: 200px;
  }
  a {
    color: #0072B2;
  }
</style>