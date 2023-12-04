<script>
    import { onMount } from "svelte";
    import { fade } from "svelte/transition";
    import Typewriter from 'svelte-typewriter'

    let greetings = ['Hello', 'नमस्ते', '안녕하세요', 'こんにちは', 'السلام عليكم', '您好', 'Hola', 'Bonjour', 'Xin chào', 'Привьет']
    let greeting = greetings[0];

    onMount( () => {
        let i = 0;
        setInterval(() => {
            greeting = greetings[i % greetings.length];
            i = i + 1;
        }, 2000);
    });
</script>

<div in:fade class="w-full h-screen flex flex-col-reverse sm:flex-row justify-center items-center p-4 gap-4" id="home">
    <div class="text-center">
        <div class="text-2xl w-full flex justify-center">
            <Typewriter class="inline">{greeting}</Typewriter><span>!</span>
        </div>
        <h1 class="md:text-5xl text-4xl font-bold">Kevin Hoffman</h1>
        <h2 class="relative md:text-4xl text-3xl opacity-80 font-semibold">AI Engineer</h2>
        <div class="flex justify-center items-center h-9 w-full gap-2 mt-2 ">
            <a href="https://www.linkedin.com/in/kemhoffman" target="_blank" class="h-full opacity-75 hover:opacity-90 transition-opacity">
                <img src="linkedin.svg" class="h-full" alt="">
            </a>
            <a href="https://github.com/KevoHoff" target="_blank" class="h-full opacity-75 hover:opacity-90 transition-opacity">
                <img src="github.svg" class="h-full" alt="">
            </a>
            
            <a href="Hoffman, Kevin.pdf" download="Hoffman, Kevin.pdf" class="px-4 py-1 h-full border-2 border-black flex justify-center items-center gap-2 rounded-full w-fit opacity-75 hover:opacity-90 transition hover:bg-gray-100">
                <img class="h-full p-1" src="download.svg" alt="" srcset="">
                <p>Resume</p>
            </a>
        </div>
        
        
    </div>
    <img class="w-1/2 max-w-sm drop-shadow-lg" src="profile2.png" alt="">
</div>