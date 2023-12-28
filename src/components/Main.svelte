<script>
  import Step from "./Step.svelte";

  let steps = [
    {name: "HotPoll", icon: "fa-solid fa-fire", link: "https://github.com/areckt/HotPoll"},
    {name: "React Course - 15 Projects", icon: "fa-brands fa-react", link: "https://github.com/areckt/React_Course_15_projects"},
    {name: "3D Animation Test Tool", icon: "fa-solid fa-cube", link: "https://github.com/areckt/3D-Animation"}
  ]
</script>

<main class="flex flex-col flex-1 p-4">
  <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
    <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
      <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
        Hi! I'm <span class="poppins text-violet-400">Arek</span> Dawid <br/>
        Frontend <span class="poppins text-violet-400">Developer</span>
      </h2>
      <p class="text-base sm:text-lg md:text-xl">
        My <span class="text-violet-400">favorite tech</span> includes JavaScript, Vue.js React.js, and TailwindCSS!
      </p>
      <a href="https://www.linkedin.com/in/adawid/" target="_blank" rel="noopener"  class="blueShadow mx-auto lg:mr-auto text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950">
        <div class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"/>
        <h4 class="relative z-9">Get in touch &rarr;</h4>
      </a>
    </div>
    <div class="relative shadow-2xl grid place-items-center">
      <img src={"images/profile.png"} alt="Profile" class="object-cover z-[2] w-[40vmin]"/>
    </div>
  </section>
  
  
  <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
    <div class="flex flex-col gap-2 text-center">
      <h6 class="text-lg sm:text-xl md:text-2xl">A few of my creative endeavors.</h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">Curious to <span class="poppins text-violet-400">see</span> my work?</h3>
    </div>
    <a href="https://github.com/areckt" target="_blank" rel="noopener" class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-violet-700 duration-200">
      <i class="fa-regular fa-circle-play"></i>
      <p>Watch the video</p>
    </a>
    <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
      <Step step={steps[0]}>
        <p>Platform for hottest polls created in <strong class="text-violet-400">Java</strong> and <strong class="text-violet-400">React.js</strong>. HotPoll is a voting platform inspired by Reditt and Twitter. The main goal of this app is to quickly share polls all around the world. It also allows to vote and check whether your side of conflict is winning 😉</p>
      </Step>
      <Step step={steps[1]}>
        <p>15 simple React projects based on a <a href="https://youtu.be/a_7Z7C_JCyo" target="_blank" rel="noopener" class="underline decoration-violet-400 hover:decoration-violet-300">
          <strong class="text-violet-400 hover:text-violet-300">tutorial by John Smilga</strong>
        </a></p>
      </Step>
      <Step step={steps[2]}>
        <p>A tool for conducting performance tests of two libraries for 3D animation in browser-based GUIs: Three.js vs Babylon.js. Project created for my engineering thesis.</p>
      </Step>
    </div>
  </section>
</main>