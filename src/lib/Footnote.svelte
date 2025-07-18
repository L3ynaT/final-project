<script>
  let { children } = $props();
</script>

<div class="footnote-text">
  <p>
    {@render children()}
  </p>
</div>

<style>
  .footnote-text {
    font-size: 0.8rem;
    font-family: "DM Sans";
    width: 50%;
    color: #000000;
    padding: 30px;
  }
</style>