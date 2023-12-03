<section class="w-full">
    <div id="experience" class="container mx-auto p-8 text-center overflow-x-hidden">
        <h2 class="h2 font-bold text-4xl">Experience</h2>
        <div id="carousel" class="w-full flex h-24 gap-16">
            <img src="Novus_Logo.png" class="shrink-0 h-full w-auto" alt="">
            <img src="Verify_Logo.jpg" class="shrink-0 h-full w-auto" alt="">
            <img src="Ursinus_College_Logo.png" class="shrink-0 h-full w-auto" alt="">
            <img src="Drexel_Logo.png" class="shrink-0 h-full w-auto" alt="">
            <div id="carousel-shadow" class="absolute w-full h-full top-0 left-0 "></div>
        </div>
    </div>
</section>

<style>
    #experience {
        animation: slide 10s linear infinite;
    }

    #carousel-shadow {
        box-shadow: 0px 0px 89px 13px rgba(0, 0, 0, 0.75) inset;
        -moz-box-shadow: 0px 0px 89px 13px rgba(0, 0, 0, 0.75) inset;
        -webkit-box-shadow: 0px 0px 89px 13px rgba(255,255,255,0.75) inset;
    }

    @keyframes slide {
        from {
            transform: translateX(0%);
        }

        to {
            transform: translateX(-100%);
        }
    }
</style>