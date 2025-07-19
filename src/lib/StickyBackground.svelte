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
.scrolly {
  position: relative;
  left: 50%;
}
.sticky {
  position: -webkit-sticky;
  position: sticky;
  top: 0;
}
</style>
