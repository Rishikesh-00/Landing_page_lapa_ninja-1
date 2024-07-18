<script>
    const hairData = [
  {
    hairType: "Brittle hair",
    description: "Hard water strips our natural oils in your hair leaving it damaged, dry, and irritated.",
    img1: "//afina.com/cdn/shop/files/Group_4128.svg?v=1698484075",
    img2: "//afina.com/cdn/shop/files/DALL_E_2023-09-18_17.52_2.png?v=1698484109&width=1500",
  },
  {
    hairType: "Damaged skin",
    description: "Hard water dries out your skin leaving it damaged, acne-prone and irritated.",
    img1: "//afina.com/cdn/shop/files/Vector_8.svg?v=1698484194",
    img2: "//afina.com/cdn/shop/files/Screenshot_2023-09-18_at_1.41_2.png?v=1698484163&width=1500"
  },
  {
    hairType: "Thinning hair",
    description: "Hard water dissolves hair lipids leaving hair less shiny, causing split ends and hair loss.",
    img1: "//afina.com/cdn/shop/files/Group_629.svg?v=1698484252",
    img2: "//afina.com/cdn/shop/files/image_34.png?v=1698484246&width=1500"
  }
];
</script>


<section class=" bg-white z-50  pt-1 ">
    <div class="bg-[#FCFBF9]  mt-20 pt-20 px-4 lg:px-20 pb-28">
        <div class="w-full    font-afina mb-6 ">
           <p class="text-2xl lg:text-[52px] lg:leading-[4rem]"> Chlorine, toxic chemicals,<br /> and heavy metals are known <br /> to
            cause:</p>
        </div>

        <!--  div for hairTypes  -->
        {#each hairData as hairData}
        <div class="flex flex-col lg:flex-row lg:justify-evenly lg:grid lg:grid-cols-3 gap-3 lg:mt-24">
            <div class=" flex flex-col gap-8 h-full ">
                <div class="">
                    <img
                        src={hairData.img1}
                        alt=""
                    />
                </div>
                <div><h1 class="text-3xl font-medium lg:text-5xl lg:font-normal">{hairData.hairType}</h1></div>
            </div>
    
    
            <div class=" h-[27rem] w-[28.2rem] ">
                <img class="object-cover  rounded-lg"
                    src={hairData.img2}
                    alt=""
                />
            </div>
    
            
            <div class="  lg:mt-16 lg:px-16  pb-4 font-semibold text-lg">
                <p>
                    {hairData.description}<br><br>
                   
                </p>
            </div>
        </div>
        {/each}


        
    </div>
</section>
