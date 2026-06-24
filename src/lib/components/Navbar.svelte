<script lang="ts">
  import { onMount } from 'svelte';

  let scrolled = $state(false);
  let menuOpen = $state(false);

  onMount(() => {
    const handler = () => { scrolled = window.scrollY > 60; };
    window.addEventListener('scroll', handler);
    return () => window.removeEventListener('scroll', handler);
  });
</script>

<nav class="fixed top-0 left-0 right-0 z-[500] flex items-center h-16 px-6 md:px-[5.16%]
            bg-black/60 backdrop-blur-xl border-b border-white/[0.04] transition-all duration-300
            {scrolled ? 'border-white/[0.08]' : ''}">

  <!-- Logo -->
  <a href="/" class="flex items-baseline gap-1 no-underline">
    <h1 class="font-display text-white text-[130%] tracking-widest leading-none">
      FYNR1X<span class="text-red mx-1">.</span>
    </h1>
    <span class="font-body text-grey text-[60%] tracking-normal">@faizeenhoque</span>
  </a>

  <!-- Desktop nav -->
  <ul class="hidden md:flex items-center ml-auto gap-6">
    <li><a href="#about"    class="font-body text-grey text-[60%] tracking-widest hover:text-red transition-colors duration-200 no-underline">ABOUT</a></li>
    <li><a href="#projects" class="font-body text-grey text-[60%] tracking-widest hover:text-red transition-colors duration-200 no-underline">PROJECTS</a></li>
    <li>
      <a href="#contact"
        class="font-body text-grey text-[60%] tracking-widest border border-red px-3 py-2
               hover:bg-red hover:text-white transition-all duration-200 no-underline">
        FIND ME
      </a>
    </li>
  </ul>

  <!-- Mobile hamburger -->
  <button
    class="md:hidden ml-auto flex flex-col gap-[5px] cursor-pointer p-1 bg-transparent border-none"
    onclick={() => menuOpen = !menuOpen}
    aria-label="Toggle menu"
  >
    <span class="block w-6 h-[1px] bg-white transition-all duration-200 {menuOpen ? 'rotate-45 translate-y-[6px]' : ''}"></span>
    <span class="block w-6 h-[1px] bg-white transition-all duration-200 {menuOpen ? 'opacity-0' : ''}"></span>
    <span class="block w-6 h-[1px] bg-white transition-all duration-200 {menuOpen ? '-rotate-45 -translate-y-[6px]' : ''}"></span>
  </button>
</nav>

<!-- Mobile menu -->
{#if menuOpen}
  <div class="fixed inset-0 z-[499] bg-black/98 backdrop-blur-xl flex flex-col items-center justify-center gap-10 md:hidden">
    {#each [['ABOUT','#about'],['PROJECTS','#projects']] as [label, href]}
      <a {href}
        class="font-display text-5xl tracking-widest text-grey hover:text-red transition-colors no-underline"
        onclick={() => menuOpen = false}>
        {label}
      </a>
    {/each}
    <a href="#contact"
      class="font-body text-[80%] tracking-widest border border-red px-8 py-3 text-red
             hover:bg-red hover:text-white transition-all no-underline"
      onclick={() => menuOpen = false}>
      FIND ME
    </a>
  </div>
{/if}