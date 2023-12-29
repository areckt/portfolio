<script>
  let tabs = [
    {name: "Projects", link: "#projects"},
    {name: "About me", link: "#about"},
    {name: "Artworks", link: "#artworks"},
  ]
</script>

<header class="px-6 flex items-center justify-between py-6 backdrop-blur-sm z-50">
  <h1 class="font-medium">
    <b class="font-bold poppins">Arek</b> Dawid
  </h1>
  <div class="sm:flex ml-auto pr-4 items-center gap-4 hidden">
    {#each tabs as tab, index}
      <a href={tab.link} class="duration-200 hover:text-sky-400">
        <p>{tab.name}</p>
      </a>
    {/each}
  </div>
  <a href="https://www.linkedin.com/in/adawid/" target="_blank" rel="noopener" class="blueShadow antialiasing relative overflow-hidden px-5 py-2 group rounded-full bg-white text-slate-950 duration-300 hover:scale-[108%] focus:ring-4 focus:ring-sky-700">
    <h4 class="relative z-9">Get in touch</h4>
  </a>
</header>