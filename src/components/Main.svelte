<script>
  import Step from "./Step.svelte";

  let steps = [
    {name: "HotPoll", icon: "fa-solid fa-fire", link: "https://github.com/areckt/HotPoll"},
    {name: "React Course - 15 Projects", icon: "fa-brands fa-react", link: "https://github.com/areckt/React_Course_15_projects"},
    {name: "3D Animation Test Tool", icon: "fa-solid fa-cube", link: "https://github.com/areckt/3D-Animation"}
  ]

  let benefits = [
    {name: "an enthusiastic frontend developer", description: "During my studies, I was forced to quickly learn the basics of React for a project from one of the courses, which I managed to achieve in less than a week. This is how my adventure with JS-based frameworks for creating web applications began.  Soon after, in the summer of 2021, I took on my first job, where this time I had to  quickly assimilate the basics of programming in Vue, which I also accomplished at a  swift pace and despite a few setbacks in the first weeks of work, after a few months I  became one of the most valuable employees of the company.  After less than a year, I received a job offer for a European Union project at the  University of Warsaw, which I of course accepted. At UW, I continued to polish my  proficiency in Vue as well as pure JS, HTML, CSS and even in the field of UI/UX design,  as I was responsible for both designing and implementing the user interface."},
    {name: "a graduate of the best polish technical university", description: "In February 2022, I obtained a bachelor’s degree in computer science from the Faculty of Electronics and Information Technology at the Warsaw University of Technology, where I am currently continuing my studies at the master’s level."},
    {name: "a hobbyist digital artist", description: "Since 2017, I have been creating digital art in my spare time using Adobe Photoshop, Illustrator and Blender."},
  ]
</script>

<main class="flex flex-col flex-1 p-4">
  <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
    <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
      <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
        Hi! I'm <span class="poppins text-sky-400">Arek</span> Dawid <br/>
        Frontend <span class="poppins text-sky-400">Developer</span>
      </h2>
      <p class="text-base sm:text-lg md:text-xl">
        My <span class="text-sky-400">favorite tech</span> includes JavaScript, Vue.js, React.js, and TailwindCSS!
      </p>
      <a href="https://www.linkedin.com/in/adawid/" target="_blank" rel="noopener"  class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950">
        <div class="absolute top-0 right-full w-full h-full bg-sky-400 opacity-20 group-hover:translate-x-full z-0 duration-200"/>
        <h4 class="relative z-9">Get in touch &rarr;</h4>
      </a>
    </div>
    <div class="relative shadow-2xl grid place-items-center">
      <img src={"images/profile.png"} alt="Profile" class="object-cover z-[2] w-[35vw]"/>
    </div>
  </section>
  
  
  <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
    <div class="flex flex-col gap-2 text-center">
      <h6 class="text-lg sm:text-xl md:text-2xl">A few of my creative endeavors.</h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">Curious to <span class="poppins text-sky-400">see</span> my work?</h3>
    </div>
    <a href="https://github.com/areckt" target="_blank" rel="noopener" class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-sky-700 duration-200">
      <i class="fa-brands fa-github"></i>
      <p>Check out my GitHub profile</p>
    </a>
    <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
      <Step step={steps[0]}>
        <p>Platform for hottest polls created in <strong class="text-sky-400">Java</strong> and <strong class="text-sky-400">React.js</strong>. HotPoll is a voting platform inspired by Reditt and Twitter. The main goal of this app is to quickly share polls all around the world. It also allows to vote and check whether your side of conflict is winning 😉</p>
      </Step>
      <Step step={steps[1]}>
        <p>15 simple React projects based on a <a href="https://youtu.be/a_7Z7C_JCyo" target="_blank" rel="noopener" class="underline decoration-sky-400 hover:decoration-sky-300">
          <strong class="text-sky-400 hover:text-sky-300">tutorial by John Smilga</strong>
        </a></p>
      </Step>
      <Step step={steps[2]}>
        <p>A tool for conducting performance tests of two libraries for 3D animation in browser-based GUIs: Three.js vs Babylon.js. Project created for my engineering thesis.</p>
      </Step>
    </div>
  </section>
  <section id="about" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 realtive">
    <div class="flex flex-col gap-2 text-center relative py-4 before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-sky-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-sky-700">
      <h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">A bit <span class="poppins text-sky-400">about</span> me.</h3>
    </div>
    <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">I am ...</p>
    <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
      {#each benefits as benefit, index}
      <div class="flex gap-6 sm:gap-8">
        <p class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold">
          0{index + 1}
        </p>
        <div class="flex flex-col gap-6 sm:gap-8">
          <h3 class="text-2xl sm:text-3xl md:text-5xl">{benefit.name}</h3>
          <p>{benefit.description}</p>
        </div>
      </div>
      {/each}
    </div>
  </section>
</main>