<script>
  import Step from "./Step.svelte";
  import ImageCard from "./ImageCard.svelte";

  let steps = [
    {name: "HotPoll", icon: "fa-solid fa-fire", link: "https://github.com/areckt/HotPoll"},
    {name: "React Course - 15 Projects", icon: "fa-brands fa-react", link: "https://github.com/areckt/React_Course_15_projects"},
    {name: "3D Animation Test Tool", icon: "fa-solid fa-cube", link: "https://github.com/areckt/3D-Animation"}
  ]

  let qualities = [
    { name: "an enthusiastic frontend developer", 
      description: [
        [
          {classes: "", text: "During my studies, I was forced to quickly learn the basics of "},
          {classes: "font-semibold text-sky-400", text: "React"},
          {classes: "", text: " for a project from one of the courses, which I managed to achieve in less than a week. This is how my adventure with JS-based frameworks for creating web applications began."},
        ],
        [
          {classes: "", text: "Soon after, in the summer of 2021, I took on my first job, where this time I had to  quickly assimilate the basics of programming in "},
          {classes: "font-semibold text-sky-400", text: "Vue.js"},
          {classes: "", text: ", which I also accomplished at a  swift pace and despite a few setbacks in the first weeks of work, after a few months I  became one of the most valuable employees of the company."},
        ],
        [
          {classes: "", text: "After less than a year, I received a job offer for a European Union project at the  University of Warsaw, which I of course accepted. At UW, I continued to polish my proficiency in "},
          {classes: "font-semibold text-sky-400", text: "Vue.js"},
          {classes: "", text: " as well as pure "},
          {classes: "font-semibold text-sky-400", text: "JS"},
          {classes: "", text: ", "},
          {classes: "font-semibold text-sky-400", text: "HTML"},
          {classes: "", text: ", "},
          {classes: "font-semibold text-sky-400", text: "CSS"},
          {classes: "", text: " and even in the field of "},
          {classes: "font-semibold text-sky-400", text: "UI/UX design"},
          {classes: "", text: ",  as I was responsible for both designing and implementing the user interface."},
        ]
      ],
    },
    { name: "a graduate of the best Polish technical university", 
      description: [
        [
          {classes: "", text: "In February 2022, I obtained a bachelor's degree in computer science from the Faculty of Electronics and Information Technology at the "},
          {classes: "font-semibold text-sky-400", text: "Warsaw University of Technology"},
          {classes: "", text: ", where I am currently continuing my studies at the master's level."},
        ]
      ],
    },
    { name: "a hobbyist digital artist", 
      description: [
        [
          {classes: "", text: "I started my journey with digital art sometime in 2017. Since then I've learned "},
          {classes: "font-semibold text-sky-400", text: "Adobe Photoshop"},
          {classes: "", text: " and "},
          {classes: "font-semibold text-sky-400", text: "Illustrator"},
          {classes: "", text: " - generally mostly 2D though recently I've been playing more and more with 3D using "},
          {classes: "font-semibold text-sky-400", text: "Blender"},
          {classes: "", text: "."},
        ],
        [
          {classes: "", text: "As for now, my forte is creating natural landscapes but in the future I'd like to expand my skills with drawing characters, machines, architecture and other fun stuff! You can check some of my artworks in the section below."},
        ]
      ]
    },
  ]

  let imagesData = [
    {title: "Tropical Village", description: "This is the first artwork that I used a mix of 2D and 3D to create.", link: "https://www.artstation.com/artwork/zOGROZ", imgUrl: "https://cdna.artstation.com/p/assets/images/images/037/256/498/large/arkadiusz-areckt-dawid-tropical-village-final.jpg?1619903882"},
    {title: "Into the Light", description: "The Light always awakens with the last breath.", link: "https://www.artstation.com/artwork/Oo0KN6", imgUrl: "https://cdna.artstation.com/p/assets/images/images/037/268/700/large/arkadiusz-areckt-dawid-into-the-light-final.jpg?1619952349"},
    {title: "Temple at the Edge of the World", description: "A temple at the edge of the world. Few knew about this ancient place. Even fewer had seen it with their eyes.", link: "https://www.artstation.com/artwork/EL0dmK", imgUrl: "https://cdnb.artstation.com/p/assets/images/images/037/268/549/large/arkadiusz-areckt-dawid-temple-at-the-edhe-of-the-world-final.jpg?1619951776"},
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
      <a href="https://www.linkedin.com/in/adawid/" target="_blank" rel="noopener noreferrer"  class="blueShadow antialiasing mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 duration-300 hover:scale-[108%] focus:ring-4 focus:ring-sky-700">
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
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">Curious to <span class="poppins text-sky-400">see</span> my work?</h3>
    </div>
    <div class="flex flex-col gap-4 -mb-4 sm:-mb-0 -mt-10">
      <a href="https://github.com/areckt" target="_blank" rel="noopener noreferrer" class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 hover:border-sky-700 duration-200 backdrop-blur-sm focus:ring-4 focus:ring-sky-700">
        <i class="fa-brands fa-github"></i>
        <p>Check out my GitHub profile</p>
      </a>
      <a href="https://codepen.io/areckt" target="_blank" rel="noopener noreferrer" class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 hover:border-sky-700 duration-200 backdrop-blur-sm focus:ring-4 focus:ring-sky-700">
        <i class="fa-brands fa-codepen"></i>
        <p>Check out my CodePen profile</p>
      </a>
    </div>
    <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
      <Step step={steps[0]}>
        <p>Platform for the hottest polls created in <strong class="text-sky-400">Java</strong> and <strong class="text-sky-400">React.js</strong>. HotPoll is a voting platform inspired by Reditt and Twitter. The main goal of this app is to quickly share polls all around the world. It also allows to vote and check whether your side of conflict is winning 😉. Project created for a university course.</p>
      </Step>
      <Step step={steps[1]}>
        <p>15 simple React projects based on a <a href="https://youtu.be/a_7Z7C_JCyo" target="_blank" rel="noopener noreferrer" class="underline decoration-sky-400 hover:decoration-sky-300">
          <strong class="text-sky-400 hover:text-sky-300">course by John Smilga</strong>.
        </a></p>
      </Step>
      <Step step={steps[2]}>
        <p>A tool for conducting performance tests of two libraries for 3D animation in browser-based GUIs: <strong class="text-sky-400 hover:text-sky-300">Three.js</strong> vs <strong class="text-sky-400 hover:text-sky-300">Babylon.js</strong>. Project created for my engineering thesis.</p>
      </Step>
    </div>
  </section>
  
  
  <section id="about" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 realtive">
    <div class="flex flex-col gap-2 text-center relative py-4 before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-sky-700 before:rounded-full after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-sky-700 after:rounded-full">
      <h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">A bit <span class="poppins text-sky-400">about</span> me.</h3>
    </div>
    <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">I am...</p>
    <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
      {#each qualities as quality, index}
      <div class="flex gap-6 sm:gap-8">
        <p class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold">
          0{index + 1}
        </p>
        <div class="flex flex-col gap-6 sm:gap-8">
          <h3 class="text-2xl sm:text-3xl md:text-5xl">{quality.name}</h3>
          {#each quality.description as paragraph}
            <p>
              {#each paragraph as fragment}
                <span class={fragment.classes}>{fragment.text}</span>
              {/each}
            </p>
          {/each}
        </div>
      </div>
      {/each}
    </div>
  </section>


  <section id="artworks" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 realtive">
    <div class="flex flex-col gap-2 text-center relative py-4 before:absolute before:top-0 before:right-0 before:w-2/3 before:h-1.5 before:bg-sky-700 before:rounded-full after:absolute after:bottom-0 after:left-0 after:w-2/3 after:h-1.5 after:bg-sky-700 after:rounded-full">
      <h6 class="text-lg sm:text-xl md:text-2xl">Want to see more?</h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">Take a look at <span class="poppins text-sky-400">some</span> of my artworks!</h3>
    </div>
    <div class="flex flex-col gap-4">
      <div class="grid gap-4 p-4 w-full mx-auto lg:grid-cols-3">
        {#each imagesData as imgData, index}
        <ImageCard imgData={imgData} />
        {/each}
      </div>
      <a href="https://areckt.artstation.com/" target="_blank" rel="noopener noreferrer" class="mx-auto px-4 py-2 -mb-4 sm:-mb-0 rounded-md border border-solid border-white flex items-center gap-2 hover:border-sky-700 duration-200 backdrop-blur-sm focus:ring-4 focus:ring-sky-700">
        <i class="fa-brands fa-artstation"></i>
        <p>Check out my ArtStation profile</p>
      </a>
    </div>
  </section>
</main>