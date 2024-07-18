<script>
    let main;
    let cursor;
    function mouseHover(dets) {
        gsap.to(cursor, {
            x: dets.x,
            y: dets.y,
            duration: 1,
            eas2: "back.out",
            top: 0,
            left: 0,
        });
    }
   
</script>

<div class="bg-black w-screen h-screen relative p-10 overflow-x-hidden">
    <div
        class="h-full w-full over bg-blue-400"
        bind:this={main}
        on:mousemove={mouseHover}
        
        role="button"
        tabindex="0"
    >
        <img
            src="https://afina.com/cdn/shop/files/Screenshot_2023-12-03_at_1.10.10_PM.png?v=1701627044&width=3840"
            class="lg:hidden"
            alt=""
        />
        <img
            class="rounded-md hidden lg:block w-full h-full object-cover"
            src="https://afina.com/cdn/shop/files/Screenshot_2023-12-03_at_1.03.19_PM.png?v=1701626658&width=3840"
            alt="water"
        />
    </div>
<!-- draggable div -->
    <div
        class="play w-32 h-32 bg-white absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 rounded-full flex justify-center items-center"
        bind:this={cursor}
    >
        <div class="w-16 h-16 flex items-center justify-center">
            <div
                class="border-l-[20px] border-l-transparent border-b-[40px] border-b-black border-r-[20px] border-r-transparent"
            ></div>
        </div>
    </div>
</div>
