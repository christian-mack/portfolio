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
    <div class="flex flex-col lg:justify-center text-center">
      <h2 class="font-semibold text-4xl sm:text-5xl md:text-8xl">
        <span class="poppins text-green-400">I'm Christian,</span> a motivated
        <span class="text-violet-400">full stack developer</span> that loves javascript.
      </h2>
      <Button
        href="#contact"
        target="_blank"
        variant="outline"
        class="mx-auto lg:mr-auto text-base sm:text-lg md:text-xl poppins relative rounded-full bg-white text-slate-950 mt-10"
        >Get in touch &rarr;</Button
      >
    </div>
  </section>

  <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
    <div class="flex gap-2 text-center">
      <div class="flex w-3/5">
        <h3 class="font-semibold text-4xl sm:text-5xl md:text-6xl text-start">
          Design that sparks engagement and inspires action.
        </h3>
      </div>
      <div class="flex flex-col w-2/5">
        <p class="text-lg sm:text-xl mb-8">
          I'm a full stack developer who specializes in building (and
          occasionally designing) exceptional digital experiences. Currently,
          I'm focused on building accessible, human-centered products at
          <a
            href="https://www.maverickdigital.xyz/"
            target="_blank"
            class="text-green-400">Maverick Digital Solutions</a
          >
          for a variety of clients.
        </p>
        <Button href="/about">About me</Button>
      </div>
    </div>

    <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
      <Step step={steps[0]}>
        <p>
          The store is a merchandising store created with <strong
            class="text-green-400"
            >Next.js Commerce.js Stripe & Node.js + Express.js!</strong
          > Commerce.js is a product CMS and Stripe is used for all transaction handling.
        </p>
      </Step>
      <Step step={steps[1]}>
        <p>
          The store is a merchandising store created with <strong
            class="text-green-400"
            >Next.js Commerce.js Stripe & Node.js + Express.js!</strong
          > Commerce.js is a product CMS and Stripe is used for all transaction handling.
        </p></Step
      >
      <Step step={steps[2]}>
        <p>
          The store is a merchandising store created with <strong
            class="text-green-400"
            >Next.js Commerce.js Stripe & Node.js + Express.js!</strong
          > Commerce.js is a product CMS and Stripe is used for all transaction handling.
        </p>
      </Step>
    </div>
  </section>
</main>
