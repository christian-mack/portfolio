<script>
  import { Button } from "$components/ui/button";
  import AboutImage from "$lib/assets/aboutplaceholder.jpeg";
  import ScrollText from "./ScrollText.svelte";
</script>

<section id="about" class="py-12">
  <div><p class="text-xl font-medium mb-1">About Me</p></div>
  <div class="flex">
    <h1 class="text-8xl font-semibold">
      Passionate developer on a <span class="text-slate-400">mission</span>
    </h1>

    <div class="flex flex-col justify-between items-end">
      <p class="text-xl">
        I'm Christian, a Full Stack Developer roaming the globe, and I focus on
        developing digital experiences that are easy to use, enjoyable, and get
        the job done.
      </p>

      <Button
        href="/contact"
        target="_blank"
        variant="ghost"
        class="w-fit text-base sm:text-lg md:text-xl relative rounded-full py-8 px-10 bg-green-600 text-slate-950 mt-14"
        >Let's Talk &rarr;</Button
      >
    </div>
  </div>
  <div class="py-12">
    <img src={AboutImage} alt="randomly generated" class="rounded-[24px]" />
  </div>
  <ScrollText />
  <div>
    <h3>My Experience</h3>
  </div>
</section>
