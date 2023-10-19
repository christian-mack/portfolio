<script>
  import { Button } from "$components/ui/button";
  import { data } from "$lib/data.ts";
  import { ChevronsRight } from "lucide-svelte";
</script>

<section class="py-20 px-4">
  <h1
    class="text-5xl md:text-7xl lg:text-8xl xl:text-9xl text-center font-semibold mb-20"
  >
    What I've been <span class="text-green-500">working on</span> so far
  </h1>
  <div class="w-full">
    <div
      class="grid grid-cols-1 lg:grid-cols-2 lg:[&>*:nth-child(3n)]:col-span-2 gap-10"
    >
      {#each data as project}
        <div class="grid col-span-1">
          <div
            class="bg-slate-600 rounded-2xl max-h-[350px] overflow-hidden w-full"
          >
            <img
              src="https://picsum.photos/500/400"
              alt="random"
              class="cover w-full"
            />
          </div>
          <div class="flex justify-between mt-8 items-center">
            <div class="flex flex-col justify-between">
              <p class="text-2xl text-slate-300">{project.title}</p>
              <div class="flex gap-4">
                {#each project.tags as tag}
                  <p class="text-md text-green-600">{tag}</p>
                {/each}
              </div>
            </div>
            <Button href={project.github} variant="ghostGreen" class="lg:p-8"
              ><ChevronsRight /></Button
            >
          </div>
        </div>
      {/each}
    </div>
  </div>
</section>
