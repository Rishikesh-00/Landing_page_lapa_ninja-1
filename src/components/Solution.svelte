<script>
    import { onMount } from 'svelte';
  
    let mediaContainer;
    let media1 ;
      let media2 ;
      let media3 ;
    onMount(() => {
      gsap.registerPlugin(ScrollTrigger);
  
    //   let media1 ;
    //   let media2 ;
    //   let media3 ;
  
      const tl = gsap.timeline({
        scrollTrigger: {
          trigger: mediaContainer,
          start: "top center",
          end: "bottom center",
          scrub: 1,
          toggleActions: "play none none reverse"
        }
      });
  
      tl.to(media1, { yPercent: -20, ease: "none" }, 0)
        .to(media2, { yPercent: 10, ease: "none" }, 0)
        .to(media3, { yPercent: 20, ease: "none" }, 0);
  
      // Initial fade-in animation
      gsap.from([media1, media2, media3], {
        opacity: 0,
        y: 50,
        duration: 1,
        stagger: 0.2,
        ease: "power3.out"
      });
    });
  </script>
  
  <section class="bg-white px-8 py-10 lg:px-16 lg:py-2">
    <div class="mt-16 lg:grid grid-cols-2 lg:px-32 lg:py-24 border border-black rounded-2xl p-4">
      <div class="div1">
        <h1 class="font-afina text-[4.5rem]">The <br /> Solution</h1>
        <p class="text-3xl font-afina">
          The A-01 shower head uses powerful filtration particles to
          capture harmful substances in your water.
        </p>
      </div>
  
      <div bind:this={mediaContainer} class="my-16 div2 h-96 flex flex-col justify-center items-center relative">
        <img bind:this={media1}
          class="media_1 absolute h-[30.3rem]"
          src="//afina.com/cdn/shop/files/Afina-0031-3.0-TOP.png?v=1700752801"
          alt="animated_image"
        />
        <img bind:this={media2}
          class="media_2 absolute h-[30.3rem]"
          src="//afina.com/cdn/shop/files/1-_1_1.png?v=1700754440"
          alt="animated_image"
        />
        <img bind:this={media3}
          class="media_3 absolute h-[30.3rem]"
          src="//afina.com/cdn/shop/files/Afina-0031-3.0-BOTTOM.png?v=1700752800"
          alt="animated_image"
        />
      </div>
  
      <div class="flex flex-col gap-6 mt-3 div3 lg:-mt-36">
        <button class="bg-[#FFEB02] w-44 px-3 py-2 rounded-md font-bold flex justify-center items-center group">
          SHOP NOW <i class="bx bxs-chevron-right text-2xl transition-transform duration-300 ease-in-out transform group-hover:translate-x-1"></i>
        </button>
        <p class="text-[15px] font-afina">
          The A-01 is designed and tested to exceed all NSD standards. It
          fits all standard showers in the USA and takes less than five
          minutes to install.
        </p>
      </div>
    </div>
  </section>

  <section class="bg-white px-8 py-10 lg:px-16 lg:py-2">
    <div class="flex flex-col lg:grid grid-cols-3 lg:mt-36 pb-12">
        <div class="col-span-3 relative">
            <h1 class="font-afina text-[2.5rem] lg:text-[4.5rem] relative z-20">Meet the A-01 <br> Filtered Shower <br> Head</h1>
        </div>
        <div class="lg:absolute lg:h-[rem] lg:w-[36rem] lg:right-[30rem] lg:mt-40 relative z-10">
            <img src="https://afina.com/cdn/shop/files/Afina-0066-1-Final.jpg?v=1700684329" alt="">
        </div>
        <!-- <div></div> -->
        <div class="flex flex-col gap-3  text-sm  lg:mt-32">
            <h1 class="text-lg font-afina">Filter out harmful substances in your water <br class="hidden lg:flex"> like:</h1> 
            <!-- small divs -->
            <div class="bg-[#F3F3F1] rounded-lg flex justify-center items-center w-36 py-3 gap-2 ">
                <img class="h-7" src="https://afina.com/cdn/shop/files/DALL_E_2023-09-18_14.11_1_bb2073f1-95e3-4f11-bad8-b9b25a586b29.png?v=1699982531" alt="">
                <span class=" text-[10px] ">CHEMICALS</span>
            </div>
            <div class="bg-[#F3F3F1] rounded-lg flex justify-center items-center w-40 py-3 gap-2 ">
                <img class="h-7" src="https://afina.com/cdn/shop/files/DALL_E_2023-09-18_16.38_1.png?v=1698149483" alt="">
                <span class="  text-[10px] ">HEAVY METALS</span>
            </div>
            <div class="bg-[#F3F3F1] rounded-lg flex justify-center items-center w-36 py-3 gap-2 ">
                <img class="h-7" src="https://afina.com/cdn/shop/files/image_128_10.png?v=1699982565" alt="">
                <span class="  text-[10px] ">CHLORINE</span>
            </div>
        </div>
        <div></div>
        <div class="mt-12 flex flex-col gap-6 z-20 lg:mt-52">
            <h1 class="font-afina text-[2.5rem] ">Get cleaned up <br class="hidden lg:flex">
                like never before.</h1>
                <button
                class="bg-[#FFEB02] w-44 px-3 py-2 rounded-md font-bold flex justify-center items-center group"
            >
                SHOP NOW <i
                    class="bx bxs-chevron-right text-2xl transition-transform duration-300 ease-in-out transform group-hover:translate-x-1"
                ></i>
            </button>
        </div>
    </div>
</section>