<script>
  import { onMount } from "svelte";
  let { title, title2, subtitle } = $props();
  let typingEffect = $state(false);

  function typewriter(node, { speed = 1 }) {
    const valid =
      node.childNodes.length === 1 &&
      node.childNodes[0].nodeType === Node.TEXT_NODE;

    if (!valid) {
      throw new Error(
        `This transition only works on elements with a single text node child`
      );
    }

    const text = node.textContent;
    const duration = text.length / (speed * 0.02);

    return {
      duration,
      tick: (t) => {
        const i = Math.trunc(text.length * t);
        node.textContent = text.slice(0, i);
      },
    };

    return {};
  }

  onMount(() => {
    typingEffect = true;
  });
</script>

<div class="title-card">
  <div class="layer"></div>
  <div class="content">
    <h1>{title}</h1>
    <h1>{title2}</h1>
    {#if typingEffect}
      <p transition:typewriter>{subtitle}</p>
    {/if}
  </div>
</div>

<style>
  .title-card {
    background-image: url("https://images.pexels.com/photos/40568/medical-appointment-doctor-healthcare-40568.jpeg");
    background-size: cover; /* resize bg image to fit */
    box-shadow: inset 0 0 0 100vh rgba(224, 224, 224, 0.7); /* slightly transparent gray layer on top of image */
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: left;
    box-sizing: border-box;
  }

  .content {
    max-width: 1100px;
    font-family: "DM Sans";
    padding: 2rem;
  }

  h1 {
    font-size: 3rem;
    font-family: "DM Serif Display";
    margin: 0;
    color: transparent;
    animation-name: fade-in;
    animation-duration: 3s;
    animation-fill-mode: forwards;
  }

  @keyframes fade-in {
    from {
      color: transparent;
    }
    to {
      color: black;
    }
  }

  p {
    font-size: 1.3rem;
    color: #005888;
    margin-top: 1rem;
    animation-name: fade-in-blue;
    animation-duration: 5s;
    animation-fill-mode: forwards;
  }

  @keyframes fade-in-blue {
    from {
      color: transparent;
    }
    to {
      color: 005888;
    }
  }

  @media (max-width: 600px) {
    h1 {
      font-size: 2.2rem;
    }

    p {
      font-size: 1.1rem;
    }
  }
</style>
