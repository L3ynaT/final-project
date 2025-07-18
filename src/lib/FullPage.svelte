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

  p {
    margin: 50vh auto;
    width: 50%;
    height: 300px;
    background-color: #E6E6E6;
    color: #000000;
    padding: 20px;
  }
</style>