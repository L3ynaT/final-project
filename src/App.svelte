<script>
  import LeftAlignedExample from "./sections/LeftAlignedExample.svelte";
  import RightAlignedExample from "./sections/RightAlignedExample.svelte";
  import ImageExample from "./sections/ImageExample.svelte";
  import TitleSection from "./sections/TitleSection.svelte";
  import InteresectionObserverBasicExample from "./sections/InteresectionObserverBasicExample.svelte";
  import IntersectionObserverAlertExample from "./sections/IntersectionObserverAlertExample.svelte";
  import DisappearingDuckExample from "./sections/DisappearingDuckExample.svelte";
  import IntersectionObserverSectionCard from "./sections/IntersectionObserverSectionCard.svelte";
  import IntersectionObserverListExample from "./sections/IntersectionObserverListExample.svelte";
  import TestSection from "./sections/TestSection.svelte";
  import StandAlone from "./sections/StandAlone.svelte";
  import CountyTitleSection from "./sections/CountyTitleSection.svelte";
  import BarChartScroll from "./sections/BarChartScroll.svelte";
</script>

<main>
  <TitleSection />
  <StandAlone />
  <CountyTitleSection />
  <BarChartScroll />

  <RightAlignedExample />
  <LeftAlignedExample />
  <ImageExample />

  <IntersectionObserverSectionCard />
  <InteresectionObserverBasicExample />
  <IntersectionObserverAlertExample />
  <DisappearingDuckExample />
  <IntersectionObserverListExample />
  <TestSection />
</main>
