<script>
  import { Button } from "$components/ui/button";
</script>

<section class="flex items-center justify-center w-full bg-slate-900">
  <div class="w-full flex flex-col items-center my-20">
    <ul class="flex justify-between gap-2 lg:gap-8 text-green-500">
      <li><a href="/about" class="hover:text-slate-200">ABOUT ME</a></li>
      <li><a href="/projects" class="hover:text-slate-200">PROJECTS</a></li>
      <li><a href="/contact" class="hover:text-slate-200">CONTACT</a></li>
    </ul>

    <h3 class="text-2xl lg:text-8xl max-w-6xl text-center font-semibold my-12">
      Want to create something awesome?
    </h3>
    <Button variant="ghostGreen" href="/contact" class="py-8 px-10  mt-2"
      >Let's Talk</Button
    >
  </div>
</section>
