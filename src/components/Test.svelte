<script>
  import { spring } from 'svelte/motion';
  import { onMount } from 'svelte';

  let scrollY;
  let innerHeight;

  const div1Y = spring(0);
  const div3Y = spring(0);

  function updatePosition() {
    const scrollPercentage = scrollY / (document.body.scrollHeight - innerHeight);
    div1Y.set(-scrollPercentage * 200);
    div3Y.set(scrollPercentage * 200);
  }

  onMount(() => {
    updatePosition(); // Initial call to set positions
    window.addEventListener('scroll', updatePosition);
    window.addEventListener('resize', updatePosition);

    return () => {
      window.removeEventListener('scroll', updatePosition);
      window.removeEventListener('resize', updatePosition);
    };
  });

  $: if (scrollY !== undefined) updatePosition();
</script>

<svelte:window bind:scrollY bind:innerHeight />

<div class="main w-full justify-center items-center flex-col gap-5 h-screen bg-blue-500 relative">
  <div 
    class="div1 flex justify-center items-center w-44 h-44 bg-yellow-500 absolute"
    style="transform: translateY({$div1Y}px);"
  >
    1
  </div>
  <div class="div2 flex justify-center items-center w-44 h-44 mt-[12rem] bg-green-500 absolute">
    2
  </div>
  <div 
    class="div3 flex justify-center items-center w-44 h-44 mt-[24rem] bg-orange-500 absolute"
    style="transform: translateY({$div3Y}px);"
  >
    3
  </div>
</div>

<div style="height: 200vh;">
  <!-- This div creates scrollable space -->
</div>