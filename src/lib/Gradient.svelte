<script>
    let { direction } = $props();
</script>

<div class="fade {direction}">
</div>

<style>
  .up {
    font-family: "DM Sans";
    height: 100vh;
    background-image: linear-gradient(rgba(255,0,0,0), rgba(148,203,236,1));
  }

  .down {
    font-family: "DM Sans";
    height: 100vh;
    background-image: linear-gradient(rgba(148,203,236,1), rgba(255,0,0,0));
  }
</style>