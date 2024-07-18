
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

<section class="sticky top-28 lg:flex items-center -z-10  lg:px-12">
    <div
        class=" flex flex-col gap-10 mt-4 px-4 lg:justify-center lg:h-[calc(100vh-7rem)]"
    >
        <h1 class="text-4xl lg:text-5xl">
            The truth is, your shower <br /> water is dirty.
        </h1>
        <button
            class="bg-[#FFEB02] w-44 px-3 py-2 rounded-md font-bold flex justify-center items-center group"
        >
            LEARN MORE <i
                class="bx bxs-chevron-right text-2xl transition-transform duration-300 ease-in-out transform group-hover:translate-x-1"
            ></i>
        </button>
    </div>
    <div class="flex justify-center items-center ">
        <img
            class="w-80 h-80 -z-10 lg:h-[34rem] lg:w-[34rem] "
            src="https://afina.com/cdn/shop/files/banner1_2e647056-afdf-42ba-ae98-4c9e8f8b3b92.png?v=1701409436"
            alt=""
        />
    </div>
    <h1 class="text-4xl mt-5 ml-4 lg:hidden">Engineered Clean</h1>
</section>

<!-- 2nd section -->
<div class="bg-white  border-black border-t-2  w-full h-screen overflow-y-hidden relative p-4 overflow-x-hidden">
    <h1 class="text-4xl ml-4 mb-10">What we do in 30 seconds:</h1>
  <div
      class="h-full w-full over"
      bind:this={main}
      on:mousemove={mouseHover}
      
      role="button"
      tabindex="0"
  >
      <img
          src="https://afina.com/cdn/shop/files/Screenshot_2023-12-03_at_1.10.10_PM.png?v=1701627044&width=3840"
          class="lg:hidden object-cover w-full h-full"
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



  
  

