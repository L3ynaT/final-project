<script>
  // `layout` can be either "right" or "left"
  // `sticky` and `scrolly` are the snippets passed in (see one of the examples)
  let { layout, sticky, scrolly } = $props();
</script>

<div class="wrapper {layout}">
  <div class="sticky">
    {@render sticky()}
  </div>

  <div class="scrolly">
    {@render scrolly()}
  </div>
</div>

<style>
  .wrapper {
    background-color: #e6e6e6;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    align-items: flex-start;
  }
  .left .scrolly {
    order: 0;
  }
  .left .sticky {
    order: 1;
  }

  .right .scrolly {
    order: 1;
  }
  .right .sticky {
    order: 0;
  }

  .scrolly {
    position: relative;
    left: 50%;
    width: 50%;
  }
  .sticky {
    position: sticky;
    top: 0;
  }
</style>
