<script>
  import { Button } from "$components/ui/button";
  import * as Accordion from "$components/ui/accordion";

  let selectedProjects = [
    {
      name: "project-1",
      title: "Web Scraper",
      description:
        "Description for the project that is about this long. Perhaps a little bit longer. Such",
      tags: ["Next.js", "Node.js", "MongoDB"],
      image: "https://www.picsum.photos/800/400",
      href: "#",
    },
    {
      name: "project-2",
      title: "AI SEO Assistant",
      description:
        "Description for the project that is about this long. Perhaps a little bit longer. Such",
      tags: ["Next.js", "OpenAI", "Prisma"],
      image: "https://www.picsum.photos/800/400",
      href: "#",
    },
    {
      name: "project-3",
      title: "Portfolio",
      description:
        "Description for the project that is about this long. Perhaps a little bit longer. Such",
      tags: ["Svelte", "Shadcn", "Typescript"],
      image: "https://www.picsum.photos/800/400",
      href: "#",
    },
  ];
</script>

<section id="selected-projects" class="py-20 lg:py-32 flex flex-col">
  <div class="flex gap-2 text-center">
    <div class="flex w-3/5">
      <h3 class="font-semibold text-4xl sm:text-5xl md:text-6xl text-start">
        Design that sparks engagement and inspires action.
      </h3>
    </div>
    <div class="flex flex-col w-2/5 items-start">
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

  <div class="mt-40">
    <div
      class="flex w-full justify-between items-center border-b-2 pb-8 mb-2 border-slate-500"
    >
      <h3 class="text-4xl font-semibold">Selected projects</h3>
      <Button
        variant="ghost"
        target="_blank"
        href="/projects"
        class="rounded-full py-7 px-8 bg-green-600 hover:bg-slate-950 hover:text-green-500 hover:outline hover:outline-2 hover:outline-green-500 text-slate-950 text-lg sm:text-xl"
        >View all projects</Button
      >
    </div>
    <Accordion.Root>
      {#each selectedProjects as project}
        <Accordion.Item value={project.name}>
          <Accordion.Trigger class="text-2xl mt-4 pb-10 hover:no-underline"
            ><div class="flex w-full justify-between">
              <div class="w-3/12 text-start"><h1>{project.title}</h1></div>
              <div class="w-8/12 text-center">
                <p>
                  {project.description}
                </p>
              </div>
              <div class="w-4/12 text-end">
                {#each project.tags as tag}
                  <Button variant="ghostGreen">{tag}</Button>
                {/each}
              </div>
            </div></Accordion.Trigger
          >
          <Accordion.Content class="pt-4 pb-8">
            <div class="flex justify-center relative">
              <img
                src={project.image}
                alt={project.title}
                class="rounded-2xl w-full object-cover"
              />
              <Button
                variant="ghostGreenSolid"
                class="absolute bottom-6 right-6 p-8"
                >View Project
              </Button>
            </div>
          </Accordion.Content>
        </Accordion.Item>
      {/each}
    </Accordion.Root>
  </div>
</section>
