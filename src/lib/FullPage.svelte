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
    font-family: "DM Sans";
    height: 100vh;
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    text-align: left;
    box-sizing: border-box;
    background-color: #94CBEC;
  }
</style>