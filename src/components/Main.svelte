<script>
  import { Button } from "$components/ui/button";
  import SelectedProjects from "$components/SelectedProjects.svelte";
  import AboutSummary from "$components/AboutSummary.svelte";
</script>

<main class="flex flex-col flex-1 p-4">
  <section id="introPage" class="py-8 sm:py-14">
    <div class="flex flex-col lg:justify-center text-center">
      <h2 class="font-semibold text-4xl sm:text-5xl md:text-8xl text-slate-400">
        <span class="poppins text-green-500">I'm Christian,</span> a motivated
        <span class="text-slate-100 underline">full stack developer</span> that loves
        javascript.
      </h2>
      <div class="w-full justify-center">
        <Button
          href="mailto:christian.ak.mack@gmail.com"
          target="_blank"
          variant="ghostGreenSolid"
          class="p-8 mt-14">Get in touch &rarr;</Button
        >
      </div>
    </div>
  </section>
  <AboutSummary />
  <SelectedProjects />
</main>
