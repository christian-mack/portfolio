<script>
  import { Instagram, Github, Linkedin } from "lucide-svelte";
  import { Button } from "$components/ui/button";
</script>

<footer class="py-8 sm:py-12 md:py-20 px-12 lg:px-48 bg-black">
  <div class="flex flex-col items-center w-full">
    <div
      class="flex flex-col lg:flex-row lg:justify-between w-full items-center mb-4 mt-5 md:mb-8 md:mt-10"
    >
      <div class="flex flex-col w-full lg:w-3/5">
        <p class="text-xl md:text-3xl lg:text-5xl mb-2 font-bold">
          <b class="text-green-500">christian</b>mack
        </p>
        <p class="text-lg lg:text-xl mt-2 font-semibold text-slate-300">
          A freelance software developer roaming the 🌎
        </p>
      </div>
      <div class="flex w-full lg:w-fit gap-4 mt-2">
        <Button
          variant="ghost"
          href="https://www.linkedin.com/in/christianmack2023/"
        >
          <Linkedin />
        </Button>
        <Button variant="ghost" href="https://github.com/christian-mack"
          ><Github /></Button
        >
        <Button
          variant="ghost"
          href="https://www.instagram.com/thechristianmack"
          ><Instagram /></Button
        >
      </div>
    </div>
    <div
      class="flex justify-center lg:justify-start w-full text-xs lg:text-base mt-10"
    >
      <p class="font-light text-slate-600 text-[10px] md:text-sm">
        © 2023 Christian Mack All rights reserved.
      </p>
    </div>
  </div>
</footer>
