<div id="about" class="w-full px-6 md:px-[5.16%] py-20 bg-black-2 border-t border-b border-white/[0.06] relative overflow-hidden">

  <!-- Watermark -->
  <div class="absolute right-0 bottom-0 font-display text-[20vw] leading-none text-red/[0.025]
              pointer-events-none select-none tracking-wide">BUILDER</div>

  <div class="relative z-10 grid grid-cols-1 lg:grid-cols-2 gap-16 lg:gap-20">

    <!-- Left: text -->
    <div>
      <p class="font-body text-[10px] tracking-widest text-red mb-4">// WHO_IS_FYNR1X.RS</p>
      <h1 class="font-body font-bold leading-none mb-10
                 text-[12vw] sm:text-[9vw] md:text-7xl lg:text-8xl">
        I DON'T<br>JUST CODE.<br><span class="text-red">I ENGINEER.</span>
      </h1>

      <div class="font-body text-grey text-sm leading-[1.9] space-y-5 max-w-xl">
        <p>
          I was never satisfied just writing apps that ran on someone else's hardware. I wanted to design the
          <span class="text-white">hardware itself</span>. So I taught myself PCB routing, embedded C, and how
          to make a microcontroller do exactly what I wanted — nothing more, nothing less.
        </p>
        <p>
          I ran the <span class="text-white">STEM Club</span> at Daffodil International School as president —
          organizing workshops, getting people hands-on with real hardware, and igniting that same obsession in
          others. Community building isn't a side quest for me. It's core to who I am.
        </p>

        <!-- Quote -->
        <div class="border-l-2 border-red pl-5 py-1 font-mono text-[85%] text-white bg-red/[0.04] pr-4">
          "Whether it's a PCB layout, a C binary, or a live API parser —
          <span class="text-red">I make things from scratch.</span>"
        </div>

        <p>
          These days I'm deep in the <span class="text-white">Hack Club</span> network — a global crew of high
          school builders who ship real projects. I track every coding hour on Hackatime and contribute to
          open-source developer tools because the ecosystem deserves better.
        </p>
      </div>

      <!-- Skills -->
      <ul class="flex flex-wrap gap-2 mt-8">
        {#each ['RUST','C','PYTHON','TYPESCRIPT','PCB DESIGN','KICAD','EMBEDDED C','ARM CORTEX','NODE JS','AND MORE..'] as skill}
          <li class="border border-white/[0.06] px-2 py-1 font-body text-[60%] tracking-wider text-grey
                     hover:bg-red hover:text-white hover:border-red transition-all duration-200 cursor-default">
            {skill}
          </li>
        {/each}
      </ul>
    </div>

    <!-- Right: stat cards + community -->
    <div class="flex flex-col gap-[2px]">

      <!-- Stats -->
      {#each [
        // { icon: '🔌', num: 'PCBs',      label: 'Custom boards routed & prototyped' },
        // { icon: '🦀', num: 'RUST',      label: 'Primary systems language of choice' },
        // { icon: '⏱️', num: 'HACKATIME', label: 'Every coding hour tracked' },
      ] as s}
        <div class="group bg-card border border-white/[0.06] px-6 py-5 flex items-center gap-5
                    hover:border-red/25 transition-colors duration-300 relative overflow-hidden">
          <div class="absolute left-0 top-0 bottom-0 w-[3px] bg-red scale-y-0 group-hover:scale-y-100
                      transition-transform duration-300 origin-bottom"></div>
          <span class="text-2xl opacity-60">{s.icon}</span>
          <div>
            <div class="font-display text-red text-2xl tracking-wide leading-none">{s.num}</div>
            <div class="font-body text-grey text-[60%] tracking-widest uppercase mt-1">{s.label}</div>
          </div>
        </div>
      {/each}

      <!-- Community cards -->
      {#each [
        { title: 'Hack Club',                    sub: 'Global network of high school makers & hackers',       badge: 'Active Member 🚀' },
        { title: 'STEM Club — Daffodil Int\'l',  sub: 'Ran workshops · hands-on hardware · grew the club',    badge: 'Ex-President 🏫' },
        { title: 'Open Source Contributor',      sub: 'Developer tools · embedded libs · community projects', badge: 'Ongoing 🛠️' },
      ] as c}
        <div class="group bg-card border border-white/[0.06] px-6 py-5
                    hover:border-red/25 transition-colors duration-300">
          <div class="font-body font-semibold text-white text-sm tracking-wide mb-1">{c.title}</div>
          <div class="font-mono text-grey text-[65%]">{c.sub}</div>
          <span class="inline-block mt-3 border border-red/25 px-2 py-[2px] font-body text-red text-[55%] tracking-widest">
            {c.badge}
          </span>
        </div>
      {/each}
    </div>
  </div>
</div>