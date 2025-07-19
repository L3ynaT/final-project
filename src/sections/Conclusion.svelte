<script>
  import "highcharts/modules/exporting";
  import ArticleTextCloser from "../lib/ArticleTextCloser.svelte";
  import TitleCard from "../lib/TitleCard.svelte";
  import ScrollerStack from "../lib/ScrollerStack.svelte";
  import FullPage from "../lib/FullPage.svelte";
  import Gradient from "../lib/Gradient.svelte";

  const title = "The wealth gap is widely known, ";
  const title2 = "but what health implications could it come with?";
  const subtitle =
    "A closer look at the health disparities in Black communities";
</script>

<div>
  <FullPage>
    <ArticleTextCloser
      >While many factors may play a role in these findings, such as living
      conditions and stress, this data suggests that having a low income can be
      a factor in making access to healthcare more challenging. Affording health
      insurance can be difficult, and, even with health insurance, there may be
      more barriers to receiving healthcare due to the shortage of primary care
      health professionals in these counties. While disparities exist in many
      areas, this data suggests that Black communities may be more
      disproportionately impacted.</ArticleTextCloser
    >
  </FullPage>
</div>
