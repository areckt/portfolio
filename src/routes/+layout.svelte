<script>
  import "../app.css";
  import Header from "../components/Header.svelte";
  import Footer from "../components/Footer.svelte";

  let y;
  let innerHeight = 0;
  let innerWidth = 0;

  function goTop() {
    document.body.scrollIntoView()
  }
</script>

<div class="relative flex flex-col max-w-[1400px] mx-auto w-full text-sm sm:text-base min-h-screen">
  <div class={"fixed bottom-10 right-10 duration-200  delay-75 flex z-[10] " + (
    y > 0 ? 'opacity-full pointer-event-auto' : 'opacity-0 pointer-event-none'
  )}>
    <button on:click={goTop} class={"mr-auto aspect-square rounded-full bg-slate-900 text-sky-400 px-3 sm:px-4 hover:bg-slate-800 "+ (
      y > 0 ? 'cursor-pointer' : 'cursor-default'
    )}>
      <i class="fa-solid fa-arrow-up grid place-items-center aspect-square" />
    </button>
  </div>
  <Header y={y}/>
  <slot />
  <Footer />
</div>

<svelte:window bind:scrollY={y} bind:innerHeight bind:innerWidth />