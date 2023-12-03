<script>
    import Typewriter from 'svelte-typewriter'
    import Hero from '$lib/Hero.svelte';
    import About from '$lib/About.svelte';
    import Experience from '$lib/Experience.svelte';
    import Projects from '$lib/Projects.svelte';
    import Accomplishments from '$lib/Accomplishments.svelte';
    import Contact from '$lib/Contact.svelte';
    import Footer from '$lib/Footer.svelte';
    import Header from '$lib/Header.svelte';

    let intro_complete = true;

    function intro_transition() {
        intro_complete = true;
    }
</script>

<div class="h-full w-full bg-surface">
    {#if intro_complete}
        <Header></Header>
    {/if}
    <div class="h-screen flex flex-col justify-center items-center gap-8 container mx-auto">
        {#if intro_complete}
            <Hero></Hero>
        {:else}
            <Typewriter keepCursorOnFinish=true on:done={() => {setTimeout(intro_transition, 2000)}}>
                <h1 class="h1 font-bold text-5xl md:text-5xl lg:text-6xl">AI, can you be used for good?</h1>
            </Typewriter>
        {/if}
    </div>
    {#if intro_complete}
        <About></About>
        <Projects></Projects>
        <Experience></Experience>
        <Contact></Contact>
        <Footer></Footer>
    {/if}
</div>