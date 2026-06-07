<script>
    import Nav from "../components/Nav.svelte";
    import Footer from "../components/Footer.svelte";
</script>

<Nav/>
<slot/>
<Footer/>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,300;0,400;0,500;0,600;0,700;0,800;1,400&display=swap');

    :root {
        --red: #af1e22;
        --dark: #1c1c1e;
        --warm: #f8f5f0;
        --gray: #6b6b6b;
        --border: #e8e8e8;
    }

    :global(*) {
        font-family: "Poppins", sans-serif;
        padding: 0;
        margin: 0;
        box-sizing: border-box;
        text-decoration: none;
        color: var(--dark);
        list-style: none;
    }

    :global(html) {
        scroll-behavior: smooth;
    }

    :global(h1) {
        line-height: 118%;
        font-size: clamp(2rem, 3vw + 1rem, 3.6rem);
        font-weight: 700;
    }

    :global(h2) {
        font-size: clamp(1.4rem, 1.5vw + 0.9rem, 2rem);
        font-weight: 700;
        line-height: 130%;
    }

    :global(h4) {
        font-size: 1rem;
        font-weight: 600;
    }
</style>
