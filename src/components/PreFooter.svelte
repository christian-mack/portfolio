<script>
  import { Button } from "$components/ui/button";
</script>

<section class="flex items-center justify-center w-full bg-slate-900">
  <div class="w-full flex flex-col items-center my-20">
    <ul class="flex justify-between gap-2 lg:gap-8 text-green-500">
      <li><a href="/home" class="hover:text-slate-200">HOME</a></li>
      <li><a href="/projects" class="hover:text-slate-200">PROJECTS</a></li>
      <li><a href="/about" class="hover:text-slate-200">ABOUT ME</a></li>
    </ul>

    <h3 class="text-2xl lg:text-8xl max-w-6xl text-center font-semibold my-12">
      Want to create something awesome?
    </h3>
    <Button
      variant="ghostGreen"
      href="mailto:christian.ak.mack@gmail.com"
      class="text-xl p-8">Send me an email</Button
    >
  </div>
</section>
