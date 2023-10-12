<script lang="ts">
  import { Instagram, Github, Linkedin } from "lucide-svelte";
  import { Button } from "$components/ui/button";
</script>

<footer class="py-12 sm:py-20 px-12 lg:px-48 bg-black">
  <div class="flex flex-col items-center w-full">
    <div
      class="flex flex-col lg:flex-row justify-between items-start w-full mb-4"
    >
      <p class=" text-slate-500 text-md lg:text-2xl mb-6">
        Stay connected with me.
      </p>
      <input
        type="text"
        class="text-white w-full lg:w-1/3 bg-black border-b-2 border-slate-500 pb-4"
        placeholder="Enter your email"
      />
    </div>
    <div
      class="flex flex-col lg:flex-row lg:justify-between w-full items-center mb-8 mt-10"
    >
      <div class="flex flex-col w-full lg:w-3/5">
        <p class="text-5xl mb-2 font-bold">
          <b class="text-green-400">christian</b>mack
        </p>
        <p class="text-xl mt-2 font-semibold text-slate-300">
          A freelance software developer based in Maryland.
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
      <p class="font-light text-slate-600 text-sm">
        © 2023 Christian Mack All rights reserved.
      </p>
    </div>
  </div>
</footer>
