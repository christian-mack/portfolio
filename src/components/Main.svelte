<script lang="ts">
  import { Button } from "$components/ui/button";
  import Step from "./Step.svelte";

  let steps = [
    { name: "Portfolio", icon: "fa-solid fa-cart-shopping" },
    { name: "Ultimate Todos", icon: "fa-solid fa-list-check" },
    { name: "Pokédex", icon: "fa-solid fa-diagram-project" },
  ];
</script>

<main class="flex flex-col flex-1 p-4">
  <section id="introPage" class="py-8 sm:py-14">
    <div
      class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
    >
      <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
        Hi! I'm <span class="poppins text-violet-400">Christian</span> Mack
        <br />Full Stack <span class="poppins text-violet-400">Developer</span>
      </h2>
      <Button
        href="#contact"
        target="_blank"
        variant="outline"
        class="mx-auto lg:mr-auto text-base sm:text-lg md:text-xl poppins relative rounded-full bg-white text-slate-950"
        >Get in touch &rarr;</Button
      >
    </div>
  </section>

  <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
    <div class="flex flex-col gap-2 text-center">
      <h6 class="text-lg sm:text-xl md:text-2xl">
        A few of my creative endeavors.
      </h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        Curious to <span class="poppins text-violet-400">see</span> my work?
      </h3>
    </div>
    <a
      href="#"
      target="_blank"
      class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-violet-700 duration-200"
    >
      <i class="fa-regular fa-circle-play" />
      <p>Watch the video</p>
    </a>

    <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
      <Step step={steps[0]}>
        <p>
          The store is a merchandising store created with <strong
            class="text-violet-400"
            >Next.js Commerce.js Stripe & Node.js + Express.js!</strong
          > Commerce.js is a product CMS and Stripe is used for all transaction handling.
        </p>
      </Step>
      <Step step={steps[1]}>
        <p>
          The store is a merchandising store created with <strong
            class="text-violet-400"
            >Next.js Commerce.js Stripe & Node.js + Express.js!</strong
          > Commerce.js is a product CMS and Stripe is used for all transaction handling.
        </p></Step
      >
      <Step step={steps[2]}>
        <p>
          The store is a merchandising store created with <strong
            class="text-violet-400"
            >Next.js Commerce.js Stripe & Node.js + Express.js!</strong
          > Commerce.js is a product CMS and Stripe is used for all transaction handling.
        </p>
      </Step>
    </div>
  </section>
</main>
