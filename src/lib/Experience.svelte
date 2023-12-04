<section class="w-full px-8">
    <div id="experience" class="container mx-auto p-8 text-center overflow-x-hidden">
        <h2 class="h2 font-bold text-4xl">Experience</h2>
        <div id="carousel" class="flex h-24 w-full bg-red-500 gap-16">
            <img src="Novus_Logo.png" class=" h-full" alt="">
            <img src="Verify_Logo.jpg" class="h-full" alt="">
            <img src="Ursinus_College_Logo.png" class="h-full" alt="">
            <img src="Drexel_Logo.png" class="h-full" alt="">
            <img src="Novus_Logo.png" class="h-full" alt="">
            <img src="Verify_Logo.jpg" class="shrink-h-full" alt="">
            <img src="Ursinus_College_Logo.png" class="shrink-0 h-full" alt="">
            <img src="Drexel_Logo.png" class="shrink-0 h-full" alt="">
        </div>
    </div>
</section>

<style>
    #carousel {
        animation: slide 4s linear infinite;
    }

    @keyframes slide {
        from {
            transform: translateX(0%);
        }

        to {
            transform: translateX(-50%);
        }
    }
</style>