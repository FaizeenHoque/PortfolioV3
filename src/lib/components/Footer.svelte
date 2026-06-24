<script lang="ts">
  const year = new Date().getFullYear();

  const links = [
    { label: 'GitHub',    href: 'https://github.com/FaizeenHoque' },
    { label: 'Discord',   href: 'https://discord.com/users/fynr1x' },
    { label: 'Hack Club', href: 'https://hackclub.com' },
  ];

  const navLinks = [
    { label: 'About',    href: '#about' },
    { label: 'Projects', href: '#projects' },
    { label: 'Find Me',  href: '#contact' },
  ];
</script>

<footer class="w-full border-t border-white/[0.06] bg-black-2">

  <!-- Top -->
  <div class="px-6 md:px-[5.16%] pt-16 pb-10 border-b border-white/[0.06] relative overflow-hidden">
    <div class="absolute right-0 bottom-0 font-display text-[18vw] leading-none text-red/[0.025]
                pointer-events-none select-none tracking-wide">FYNR1X</div>

    <div class="relative z-10 flex flex-col md:flex-row md:items-end justify-between gap-10">

      <!-- Branding -->
      <div>
        <p class="font-body text-[10px] tracking-widest text-red mb-4">// END_OF_PAGE</p>
        <h2 class="font-display leading-none tracking-wide text-white
                   text-[14vw] sm:text-[10vw] md:text-[7rem] lg:text-[8rem]">
          FAIZEEN<span class="text-red">.</span>
        </h2>
        <p class="font-mono text-grey text-[70%] tracking-widest mt-3">
          @fynr1x · 🇧🇩 Dhaka, Bangladesh
        </p>
      </div>

      <!-- Links -->
      <div class="flex flex-col sm:flex-row gap-10 md:gap-16 pb-1">
        <div>
          <p class="font-body text-[58%] tracking-[0.3em] text-grey/50 uppercase mb-4">Sitemap</p>
          <ul class="flex flex-col gap-3">
            {#each navLinks as n}
              <li>
                <a href={n.href}
                  class="font-body text-[70%] tracking-widest text-grey hover:text-red
                         transition-colors duration-200 no-underline uppercase">
                  {n.label}
                </a>
              </li>
            {/each}
          </ul>
        </div>
        <div>
          <p class="font-body text-[58%] tracking-[0.3em] text-grey/50 uppercase mb-4">Find Me</p>
          <ul class="flex flex-col gap-3">
            {#each links as l}
              <li>
                <a href={l.href} target="_blank" rel="noopener noreferrer"
                  class="group font-body text-[70%] tracking-widest text-grey hover:text-red
                         transition-colors duration-200 no-underline uppercase flex items-center gap-2">
                  {l.label}
                  <span class="opacity-0 group-hover:opacity-100 transition-opacity text-red text-[80%]">↗</span>
                </a>
              </li>
            {/each}
          </ul>
        </div>
      </div>
    </div>
  </div>

  <!-- Bottom bar -->
  <div class="px-6 md:px-[5.16%] py-5 flex flex-col sm:flex-row items-center justify-between gap-3">
    <p class="font-mono text-[60%] tracking-widest text-grey/40">
      © {year} <span class="text-red">Faizeen Hoque</span>. All rights reserved.
    </p>
    <p class="font-mono text-[60%] tracking-widest text-grey/40">
      Built from scratch<span class="text-red">.</span> No templates.
    </p>
  </div>

</footer>