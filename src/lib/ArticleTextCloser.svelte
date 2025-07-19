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
    margin: 40px auto;
    font-size: 1.5rem;
    font-family: "DM Sans";
    width: 50%;
    background-color: #E6E6E6;
    color: #000000;
    padding: 30px;
  }
</style>