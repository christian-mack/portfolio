<script>
  import { Button } from "$components/ui/button";
  import { Badge } from "$components/ui/badge";
  import { data } from "$lib/data.ts";
</script>

<section
  id="selected-projects"
  class="py-2 lg:py-18 flex flex-col mb-20 md:mb-32"
>
  <div class="">
    <div class="flex w-full md:justify-between items-center md:pb-8 md:mb-2">
      <h3 class="text-3xl md:text-4xl font-semibold">Selected projects</h3>
      <Button
        variant="ghostGreen"
        target="_blank"
        href="/projects"
        class="p-8 hidden md:flex">View all projects</Button
      >
    </div>

    {#each data as project}
      <div class="text-2xl mt-4 pb-10 hover:no-underline">
        <div class="flex flex-col w-full justify-between">
          <div class="flex justify-center relative">
            <img
              src={project.image}
              alt={project.title}
              class="rounded-2xl w-full object-cover"
            />
            <div class="absolute bottom-6 left-6 gap-6">
              {#each project.tags as tag}
                <Badge
                  variant="secondary"
                  class="mr-3 md:text-sm bg-slate-200 hover:bg-slate-200 text-slate-950"
                  >{tag}</Badge
                >
              {/each}
            </div>
          </div>
          <div
            class="flex flex-col text-start md:flex-row md:items-center justify-between w-full py-8"
          >
            <div>
              <h1 class="text-3xl text-slate-300">{project.title}</h1>
              <p class="text-slate-400">
                {project.description}
              </p>
            </div>
            <div class=" text-end">
              <Button variant="ghostGreen" class="p-8" href={project.github}
                >View Project
              </Button>
            </div>
          </div>
        </div>
      </div>
    {/each}
  </div>
</section>
