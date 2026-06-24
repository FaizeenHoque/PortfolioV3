<script lang="ts">
  const projects = [
    {
      id: '01',
      title: 'FLINT_LAUNCHER',
      tags: ['TAURI', 'SVELTE'],
      description: 'A super lightweight, sleek, modern, blazing-fast Minecraft launcher designed to run effortlessly on any system, packed with powerful features, seamless updates, and a smooth, snappy interface, all built from scratch using the cutting-edge Tauri framework and the reactive Svelte frontend.',
      rating: 4,
      github: 'https://github.com/FaizeenHoque/FlintLauncher'
    },
    {
      id: '02',
      title: 'HYPRBOARD_V2',
      tags: ['KICAD', 'RP2040'],
      description: 'HyprboardV2 is a compact, RP2040-based development board and the completed successor to the original HyprboardV1 (which never saw the light of day). Built for makers who want a capable, open-source board without the corporate overhead.',
      rating: 4,
      github: 'https://github.com/FaizeenHoque/HyprboardV2'
    },
    {
      id: '03',
      title: 'CELLA-1M9E1D0B0UMX',
      tags: ['KICAD', 'RP2040', 'MECHANICAL', 'KMK'],
      description: 'A minimal 9-key macropad with rotary encoder. Custom PCB, XIAO RP2040, KMK firmware.',
      rating: 3,
      github: 'https://github.com/FaizeenHoque/CELLA-1M9E1D0B0UMX'
    },
  ];
</script>

<div id="projects" class="w-full px-6 md:px-[5.16%] py-20">

  <!-- Header -->
  <div class="flex items-end justify-between mb-14">
    <div>
      <p class="font-body text-[10px] tracking-widest text-red mb-3">// PROJECTS[]</p>
      <h1 class="font-display leading-none tracking-wide text-[12vw] sm:text-[9vw] md:text-8xl">
        THINGS I'VE<br><span class="text-red">SHIPPED.</span>
      </h1>
    </div>
    <span class="font-display leading-none text-red/10 tracking-wide select-none hidden sm:block text-[10vw] md:text-[7rem]">
      0{projects.length}
    </span>
  </div>

  <!-- Cards -->
  <div class="flex flex-col gap-[2px]">
    {#each projects as p}
      <a
        href={p.github}
        target="_blank"
        rel="noopener noreferrer"
        class="group bg-card border border-white/[0.06] hover:border-red/25
               transition-colors duration-300 no-underline flex flex-col md:flex-row"
      >
        <!-- Left: ID + accent bar -->
        <div class="flex-shrink-0 flex flex-row md:flex-col items-center justify-between md:justify-start
                    px-6 py-5 md:py-8 md:w-24 border-b md:border-b-0 md:border-r border-white/[0.06]
                    group-hover:border-red/15 transition-colors duration-300 gap-4 md:gap-0">
          <span class="font-mono text-[65%] text-grey/40 tracking-widest">{p.id}</span>
          <!-- Rating dots -->
          <div class="flex md:flex-col gap-[5px] mt-0 md:mt-auto">
            {#each Array(5) as _, i}
              <div class="w-[5px] h-[5px] rounded-full transition-colors duration-200
                          {i < p.rating ? 'bg-red' : 'bg-white/10'}"></div>
            {/each}
          </div>
        </div>

        <!-- Middle: content -->
        <div class="flex-1 px-7 py-7 flex flex-col gap-4 min-w-0">
          <h3 class="font-display text-[1.6rem] md:text-[2rem] tracking-wide leading-none text-white
                     group-hover:text-red transition-colors duration-200">
            {p.title}
          </h3>
          <p class="font-body text-grey text-[78%] leading-relaxed max-w-2xl">{p.description}</p>
          <ul class="flex flex-wrap gap-2 mt-1">
            {#each p.tags as tag}
              <li class="border border-red/25 px-2 py-[2px] font-body text-[55%] font-bold tracking-widest text-red">
                {tag}
              </li>
            {/each}
          </ul>
        </div>

        <!-- Right: arrow + github -->
        <div class="flex-shrink-0 flex flex-row md:flex-col items-center justify-between md:justify-center
                    px-6 py-5 md:py-8 md:w-20 border-t md:border-t-0 md:border-l border-white/[0.06]
                    group-hover:border-red/15 transition-colors duration-300 gap-4 md:gap-6">
          <span class="font-body text-grey text-xs tracking-widest uppercase hidden md:block rotate-90 md:rotate-0
                       group-hover:text-red transition-colors">
            VIEW
          </span>
          <span class="text-grey text-xl transition-all duration-300
                       group-hover:text-red group-hover:translate-x-1 group-hover:-translate-y-1">
            ↗
          </span>
        </div>
      </a>
    {/each}
  </div>

</div>