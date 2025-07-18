<script>
    let { title, title2, subtitle } = $props();
</script>

<div class="title-card">
    <div class="layer"></div>
    <div class="content">
        <h1>{title}</h1>
        <h1>{title2}</h1>
        <p>{subtitle}</p>
    </div>
</div>

<style>
    .title-card {
        background-image: url("https://images.pexels.com/photos/40568/medical-appointment-doctor-healthcare-40568.jpeg");
        background-size: cover;     /* resize bg image to fit */
        box-shadow: inset 0 0 0 100vh rgba(224, 224, 224, 0.7);     /* slightly transparent gray layer on top of image */
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: left;
        box-sizing: border-box;
        font-family: "Inter", sans-serif;
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
        color: #000000;
    }

    p {
        font-size: 1.3rem;
        color: #005888;
        margin-top: 1rem;
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
