<script>
  import "highcharts/modules/exporting";
  import ArticleTextCloser from "../lib/ArticleTextCloser.svelte";
  import ArticleText from "../lib/ArticleText.svelte";
  import Scroller from "../lib/Scroller.svelte";
</script>

<div>
  <Scroller layout="right">
    {#snippet sticky()}
      <div class="picture">
        <img
          src="https://images.pexels.com/photos/7163955/pexels-photo-7163955.jpeg"
          alt="USA map"
        />
      </div>
    {/snippet}

    {#snippet scrolly()}
      <div class="text">
        <ArticleText>
          In 2023, 12 of the 20 counties fell into the lower quartile of health
          insurance coverage percentage. The remaining 8 counties were in the
          second quartile.
        </ArticleText>
        <ArticleText>
          All 20 counties were in the bottom two quartiles, meaning they were
          all below the median total population percentage with health
          insurance.
        </ArticleText>
      </div>
    {/snippet}
  </Scroller>
</div>

<style>
  img {
    width: 100%;
    height: 105vh;
    object-fit: contain;
  }
  .text {
  }
</style>
