<script>
  let { children } = $props();
</script>

<div class="article-text">
  <p>
    {@render children()}
  </p>
</div>

<style>
  .article-text {
    margin: 50vh auto;
    font-size: 1.5rem;
    font-family: "DM Sans";
    width: 50%;
    background-color: #e6e6e6;
    color: #000000;
    padding: 30px;
    margin-bottom: 200px;
  }
</style>