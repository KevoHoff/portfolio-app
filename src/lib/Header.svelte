<script>
    let open = false;

    function toggleMenu() {
        open = !open;
    }
</script>

<nav class="fixed top-0 right-0 z-10"> 
    <div class="m-2 rounded-full">
        <button id="menu" class="w-8 h-6 relative m-4" class:open={open} on:click={toggleMenu}>
            <span></span>
            <span></span>
            <span></span>
        </button>
    </div>
    <a id="home_a" href="#about" class:open={open} class="z-10 absolute text-center text-lg rounded-full bg-secondary shadow">
        Home
    </a>
    <a id="about_a" href="#about" class:open={open} class="z-10 absolute text-center text-lg rounded-full bg-secondary shadow">
        About
    </a>
    <a id="projects_a" href="#projects" class:open={open} class="z-10 absolute text-center text-lg rounded-full bg-secondary shadow">
        Projects
    </a>
    <a id="contact_a" href="#contact" class:open={open} class="z-10 absolute text-center text-lg rounded-full bg-secondary shadow">
        Contact
    </a>
</nav>

<style>
    a {
        transition-property: all;
        transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
        transition-duration: 150ms;
        transform-origin: right;

        opacity: 0;

        padding: 2px 10px;
    }

    #home_a:hover{
        transform: scale(1.1);
    }

    #about_a:hover {
        transform: scale(1.1) rotate(-15deg);
    }

    #projects_a:hover {
        transform: scale(1.1) rotate(-30deg);
    }

    #contact_a:hover {
        transform: scale(1.1) rotate(-45deg);
    }

    #home_a {
        --angle: 0deg
        left: calc(-100px * cos(--angle));
        top: calc(10px + (100px * sin(--angle)));
        transition-delay: 50ms;
    }

    #home_a.open {
        opacity: 100%;
    }

    #about_a {
        left: calc(-100px * cos(15deg));
        top: calc( (100px * sin(15deg)));
        transition-delay: 50ms;
    }

    #about_a.open {
        opacity: 100%;
    }

    #projects_a {
        --angle: 30deg
        left: calc(-10px + -100px * cos(--angle));
        top: calc(10px + (100px * sin(--angle)));
        transform: rotate(-20deg);
        transition-delay: 100ms;
    }

    #projects_a.open {
        opacity: 100%;
    }

    #contact_a {
        --angle: 45deg
        left: calc(-10px + -100px * cos(--angle));
        top: calc(10px + (100px * sin(--angle)));
        transform: rotate(-40deg);
        transition-delay: 150ms;
    }

    #contact_a.open {
        opacity: 100%;
    }

    #menu span:nth-child(1) {
        top: 0px;
    }
    #menu span:nth-child(2) {
        top: 50%;
    }
    #menu span:nth-child(3) {
        top: 100%;
    }

    #menu span {
        display: block;
        position: absolute;
        right: 0;
        width: 100%;
        height: 2px;
        background-color: black;
        border-radius: 50px;

        transition-property: all;
        transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
        transition-duration: 150ms;
    }

    #menu.open span:nth-child(1) {
        transform: translateY(12px) rotate(45deg);
    }

    #menu.open span:nth-child(2) {
        opacity: 0;
    }

    #menu.open span:nth-child(3) {
        transform: translateY(-12px) rotate(-45deg);
    }
</style>