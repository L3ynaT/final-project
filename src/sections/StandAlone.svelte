<script>
  import "highcharts/modules/exporting";
  import ObservedArticleText from "../lib/ObservedArticleText.svelte";
  import Footnote from "../lib/Footnote.svelte";
  import { fade } from "svelte/transition";

  let textIsVisible = $state(false);
  const options = {
    threshold: [0.9, 1.0],
  };

  const showTextCallback = (entries, observer) => {
    entries.forEach((entry) => {
      const elem = entry.target;

      if (entry.intersectionRatio >= 0.95) {
        textIsVisible = true;
      } else if (entry.intersectionRatio < 0.95) {
      }
    });
  };
</script>

<div>
  <section>
    <article>
      {#if textIsVisible}
        <p in:fade={{duration: 1700}}>
          The impact of a lower income does not end at financial struggles.
          Having a lower income may possibly be linked to greater health risks.
        </p>
      {/if}
      <ObservedArticleText callback={showTextCallback} {options}>.</ObservedArticleText>
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

  p {
    margin: 40px auto;
    font-size: 1.5rem;
    font-family: "DM Sans";
    width: 50%;
    background-color: #e6e6e6;
    color: #000000;
    padding: 30px;
  }
</style>
