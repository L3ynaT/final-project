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
    width: 50%;
    background-color: #ff99fc;
    color: #007052;
    border: solid #8427c9 3px;
    padding: 20px;
  }
</style>
