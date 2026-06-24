<div class="w-full pt-24 px-6 md:px-[5.16%] pb-[5.16%]">

  <!-- Location pill -->
  <div class="flex justify-end mb-6">
    <div class="flex items-center gap-2 px-4 py-1 border border-white/[0.06] bg-black-2/60 backdrop-blur-md
                rounded-full text-xs tracking-widest text-grey font-body">
      <span>🇧🇩</span>
      <span>Dhaka, Bangladesh</span>
      <span class="text-red">•</span>
    </div>
  </div>

  <!-- Handle -->
  <p class="font-body text-[10px] tracking-widest text-red mb-2">> fynr1x / faizeen hoque</p>

  <!-- Name -->
  <div class="mb-6">
    <h1 class="font-display leading-none tracking-normal text-white
               text-[18vw] md:text-[13vw] lg:text-[150px]">FAIZEEN</h1>
    <div>
      <h1 class="font-display leading-none tracking-normal text-red
               text-[18vw] md:text-[13vw] lg:text-[150px]">HOQUE</h1>
      <h1 class="font-display leading-none tracking-normal
                text-[18vw] md:text-[13vw] lg:text-[150px]"
          style="-webkit-text-fill-color:transparent; -webkit-text-stroke: clamp(1px,0.3vw,5px) #555;">
        .DEV
      </h1>
    </div>
  </div>

  <!-- Role chips -->
  <ul class="flex flex-wrap gap-2 mt-5">
    {#each ['SOFTWARE ENGINEER','HARDWARE DEVELOPER','PCB DESIGNER','EMBEDDED SYSTEMS','HACK CLUB MAKER'] as role}
      <li class="border border-black-2 px-2 py-1 font-body text-[65%] text-grey
                 hover:bg-red hover:text-white hover:border-red transition-all duration-200 cursor-default">
        {role}
      </li>
    {/each}
  </ul>

  <!-- Description -->
  <p class="text-grey font-body mt-10 text-sm md:text-base leading-relaxed max-w-lg">
    I live at the intersection of <span class="text-white">code and circuitry</span>. From routing
    custom PCBs at 3am to writing <span class="text-red">low-level C</span> that talks directly
    to silicon — I don't just build software. I build the <span class="text-white">hardware it runs on.</span>
  </p>

  <!-- CTAs -->
  <div class="flex flex-wrap gap-3 pt-10">
    <a href="#projects"
      class="font-display text-white text-[80%] tracking-widest bg-red px-7 py-2
             hover:bg-white hover:text-red transition-all duration-200 no-underline">
      SEE MY WORK
    </a>
    <a href="#contact"
      class="font-display text-grey text-[80%] tracking-widest px-7 py-2
             hover:text-white transition-colors duration-200 no-underline">
      GET IN TOUCH >
    </a>
  </div>
</div>