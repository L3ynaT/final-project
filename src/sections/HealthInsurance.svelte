<script>
  import "highcharts/modules/exporting";
  import ArticleTextCloser from "../lib/ArticleTextCloser.svelte";
  import ArticleText from "../lib/ArticleText.svelte";
  import TitleCard from "../lib/TitleCard.svelte";
  import ScrollerStack from "../lib/ScrollerStack.svelte";
  import FullPage from "../lib/FullPage.svelte";
  import StickyBackground from "../lib/StickyBackground.svelte";

  const title = "The wealth gap is widely known, ";
  const title2 = "but what health implications could it come with?";
  const subtitle =
    "A closer look at the health disparities in Black communities";
</script>

<div>
  <StickyBackground layout="right">
    {#snippet sticky()}
      <img
        src="https://images.unsplash.com/photo-1446776653964-20c1d3a81b06?q=80&w=1171&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
        alt="USA map"
      />
    {/snippet}

    {#snippet scrolly()}
      <div class="text">
        <ArticleText>
          12 of the 20 counties were in the lower quartile of health insurance
          coverage percentage.
        </ArticleText>
        <ArticleText
          >The remaining 8 counties were in the second quartile. None of the
          counties were in the third or fourth quartiles.
        </ArticleText>
      </div>
    {/snippet}
  </StickyBackground>
</div>

<style>
  img {
    display: flex;
    justify-content: center;

    width: 100%;
    object-fit: cover;
  }
  .text {
    height: 100vh;
    width: 50%;
  }
</style>
