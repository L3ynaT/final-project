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
  <ArticleTextCloser>
    While many factors may play a role in these findings, such as living
    conditions and stress, this data suggests that having a low income can be a
    factor in making access to healthcare more challenging.
  </ArticleTextCloser>
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
    background-color: #94cbec;
    padding-top: 200px;
    padding-bottom: 200px;
  }
</style>