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
  <ScrollerStack layout="left">
    {#snippet sticky()}
      <TitleCard {title} {title2} {subtitle} />
    {/snippet}

    {#snippet scrolly()}
      <Gradient direction="up"></Gradient>
      <FullPage>
        <ArticleTextCloser>In 2022, the median annual earnings for Black full-time workers (25-34
        years old of all education levels) was $46,040, one of the lowest
        earnings compared to other racial/ethnic groups.</ArticleTextCloser>
        <ArticleTextCloser>[a graph will go here]</ArticleTextCloser>
      </FullPage>
    
    {/snippet}
  </ScrollerStack>
</div>
