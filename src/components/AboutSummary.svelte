<script>
  import { Button } from "$components/ui/button";
</script>

<div
  class="flex flex-col lg:flex-row gap-8 lg:gap-1 text-center my-20 lg:my-28"
>
  <div class="flex lg:w-3/5">
    <h3 class="font-semibold text-3xl sm:text-5xl md:text-6xl text-start">
      Design that sparks engagement and inspires action.
    </h3>
  </div>
  <div class="flex flex-col lg:w-2/5 items-end lg:items-start">
    <p class="text-lg sm:text-xl mb-8 text-start">
      I'm a full stack developer who specializes in building (and occasionally
      designing) exceptional digital experiences. Currently, I'm focused on
      building accessible, human-centered products at
      <a
        href="https://www.maverickdigital.xyz/"
        target="_blank"
        class="text-green-400">Maverick Digital Solutions</a
      >
      for a variety of clients.
    </p>
    <div class="flex">
      <Button
        href="/about"
        target="_blank"
        variant="ghost"
        class="mx-auto lg:mr-auto text-base sm:text-lg md:text-xl relative rounded-full py-8 px-10 outline outline-1 outline-green-500  text-green-500 hover:text-slate-950 hover:bg-green-500 mt-2"
        >About Me</Button
      >
    </div>
  </div>
</div>
