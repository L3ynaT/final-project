<script>
  import Scroller from "../lib/Scroller.svelte";
  import ArticleText from "../lib/ArticleText.svelte";
</script>

<div>
  <Scroller layout="left">
    {#snippet sticky()}
      <img
        src="https://images.unsplash.com/vector-1738590593450-647695dbf9d0?q=80&w=880&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
        alt="coding illustration"
      />
    {/snippet}

    {#snippet scrolly()}
      <ArticleText>Here is an additional piece of text!</ArticleText>

      <ArticleText>This is another piece of text.</ArticleText>

      <ArticleText>My final piece of text is here.</ArticleText>
    {/snippet}
  </Scroller>
</div>
