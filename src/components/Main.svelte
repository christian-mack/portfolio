<script lang="ts">
  import { Button } from "$components/ui/button";
  import Projects from "$components/SelectedProjects.svelte";
</script>

<main class="flex flex-col flex-1 p-4">
  <section id="introPage" class="py-8 sm:py-14">
    <div class="flex flex-col lg:justify-center text-center">
      <h2 class="font-semibold text-4xl sm:text-5xl md:text-8xl text-slate-400">
        <span class="poppins text-green-400">I'm Christian,</span> a motivated
        <span class="text-slate-100 underline">full stack developer</span> that loves
        javascript.
      </h2>
      <Button
        href="#contact"
        target="_blank"
        variant="ghost"
        class="mx-auto lg:mr-auto text-base sm:text-lg md:text-xl relative rounded-full py-8 px-10 bg-green-600 text-slate-950 mt-14"
        >Get in touch &rarr;</Button
      >
    </div>
  </section>

  <Projects />
</main>
