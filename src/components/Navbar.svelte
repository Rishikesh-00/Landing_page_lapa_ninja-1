<script>
  import { onMount } from "svelte";
  import { gsap } from "gsap";
  import { fly } from 'svelte/transition';

  let hours = 0;
  let minutes = 55;
  let seconds = 56;
  let isSidenavOpen = false;

  function startTimer() {
    const interval = setInterval(() => {
      if (seconds > 0) {
        seconds -= 1;
      } else {
        if (minutes > 0) {
          minutes -= 1;
          seconds = 59;
        } else {
          if (hours > 0) {
            hours -= 1;
            minutes = 59;
            seconds = 59;
          } else {
            clearInterval(interval);
          }
        }
      }
    }, 1000);
  }

  function toggleSidenav() {
    isSidenavOpen = !isSidenavOpen;
  }

  

  onMount(() => {
    startTimer();
    gsap.from(".nav", {
      y: -110,
      duration: 1,
    });

  
  });
</script>

<section class="flex justify-center items-center text-sm gap-4 h-12 bg-[#F4F4F2]">
  <div class="text-[12px] font-medium">
    Mystery offer Activate! See Code at Checkout
  </div>
  <div class="flex flex-col text-md font-bold">
    <div class="tracking-[.1rem]">
      {hours.toString().padStart(2, "0")}:{minutes
        .toString()
        .padStart(2, "0")}:{seconds.toString().padStart(2, "0")}
    </div>
    <div class="text-[8px] -mt-2">
      <span class="ml-1">Hrs</span> <span class="ml-2">Mine</span>
      <span class="ml-2">Secs</span>
    </div>
  </div>
</section>

<section class="nav">
  <div class="border-b lg:border-b-0 border-t flex h-16 justify-between px-6 items-center">
    <div class="flex justify-center items-center gap-4">
      <button class="group" on:click={toggleSidenav}>
        <i class="bx bx-menu text-3xl group-hover:scale-110"></i>
      </button>
      <img
        class="w-24 h-10"
        src="https://afina.com/cdn/shop/files/LogoLockup-5.svg?v=1701414542&width=150"
        alt="logo"
      />
    </div>
    <div class="flex justify-center items-center gap-4">
      <button class="bg-[#FFEB02] px-3 py-2  rounded-md  flex justify-center items-center group">
        SHOP NOW <i class='bx bxs-chevron-right text-2xl transition-transform duration-300 ease-in-out transform group-hover:translate-x-1'></i>
      </button>
      <span class="border border-black px-5 py-2 rounded-md hover:bg-black hover:text-white cursor-pointer">Cart 0</span>
    </div>
  </div>
</section>

{#if isSidenavOpen}
  <section class="absolute bg-white z-50 w-full md:w-[25rem] border-r top-12 h-[calc(100vh-3rem)] border-t px-10" transition:fly="{{ x: -250, duration: 300 }}">
    <div class="flex justify-between lg:justify-end items-center py-10">
      <img
        class="w-24 h-10 lg:hidden"
        src="https://afina.com/cdn/shop/files/LogoLockup-5.svg?v=1701414542&width=150"
        alt="logo"
      />
      <button on:click={toggleSidenav}>
        <svg width='18' height='18' xmlns="http://www.w3.org/2000/svg" aria-hidden="true" focusable="false" class="icon icon-close" fill="none" viewBox="0 0 18 17">
          <path d="M.865 15.978a.5.5 0 00.707.707l7.433-7.431 7.579 7.282a.501.501 0 00.846-.37.5.5 0 00-.153-.351L9.712 8.546l7.417-7.416a.5.5 0 10-.707-.708L8.991 7.853 1.413.573a.5.5 0 10-.693.72l7.563 7.268-7.418 7.417z" fill="currentColor"></path>
        </svg>
      </button>
    </div>
 <!-- div2 -->
<div class="font-afina text-4xl flex flex-col gap-4 mt-10">
  <ul>
    <a href="/" class="relative inline-block group">
      <span class="relative z-10">The A-01</span>
      <span class="absolute bottom-0 left-0 w-full h-0.5 bg-current origin-right transform scale-x-0 transition-transform duration-300 ease-out group-hover:scale-x-100 group-hover:origin-left"></span>
    </a>
  </ul>
  
  <ul>
    <a href="/" class="relative inline-block group">
      <span class="relative z-10">A-01 Filter</span>
      <span class="absolute bottom-0 left-0 w-full h-0.5 bg-current origin-right transform scale-x-0 transition-transform duration-300 ease-out group-hover:scale-x-100 group-hover:origin-left"></span>
    </a>
  </ul>
  <ul>
    <a href="/" class="relative inline-block group">
      <span class="relative z-10">About</span>
      <span class="absolute bottom-0 left-0 w-full h-0.5 bg-current origin-right transform scale-x-0 transition-transform duration-300 ease-out group-hover:scale-x-100 group-hover:origin-left"></span>
    </a>
  </ul>
  <ul>
    <a href="/" class="relative inline-block group">
      <span class="relative z-10">Science</span>
      <span class="absolute bottom-0 left-0 w-full h-0.5 bg-current origin-right transform scale-x-0 transition-transform duration-300 ease-out group-hover:scale-x-100 group-hover:origin-left"></span>
    </a>
  </ul>
</div>

<!-- div3 -->
<div class="font-afina text-2xl flex flex-col gap-4 mt-24">
  <ul>
    <a href="/" class="relative inline-block group">
      <span class="relative z-10">Blog</span>
      <span class="absolute bottom-0 left-0 w-full h-0.5 bg-current origin-right transform scale-x-0 transition-transform duration-300 ease-out group-hover:scale-x-100 group-hover:origin-left"></span>
    </a>
  </ul>
  <ul>
    <a href="/" class="relative inline-block group">
      <span class="relative z-10">Contact</span>
      <span class="absolute bottom-0 left-0 w-full h-0.5 bg-current origin-right transform scale-x-0 transition-transform duration-300 ease-out group-hover:scale-x-100 group-hover:origin-left"></span>
    </a>
  </ul>
  <ul>
    <a href="/" class="relative inline-block group">
      <span class="relative z-10">Account</span>
      <span class="absolute bottom-0 left-0 w-full h-0.5 bg-current origin-right transform scale-x-0 transition-transform duration-300 ease-out group-hover:scale-x-100 group-hover:origin-left"></span>
    </a>
  </ul>
</div>
  </section>
{/if}

