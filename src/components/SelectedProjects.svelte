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
      github: "https://github.com/christian-mack/web-scraper",
    },
    {
      name: "project-2",
      title: "AI SEO Assistant",
      description:
        "Description for the project that is about this long. Perhaps a little bit longer. Such",
      tags: ["Next.js", "OpenAI", "Prisma"],
      image: "https://www.picsum.photos/800/400",
      href: "#",
      github: "https://github.com/christian-mack/rank-rocket",
    },
    {
      name: "project-3",
      title: "Portfolio",
      description:
        "Description for the project that is about this long. Perhaps a little bit longer. Such",
      tags: ["Svelte", "Shadcn", "Typescript"],
      image: "https://www.picsum.photos/800/400",
      href: "#",
      github: "https://github.com/christian-mack/portfolio",
    },
  ];

  let active = false;

  function toggle() {
    console.log("BEFORE: ", active);
    active = !active;
    console.log("AFTER: ", active);
  }
</script>

<section id="selected-projects" class="py-5 lg:py-18 flex flex-col mb-32">
  <div class="">
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
    <Accordion.Root value={"project-1"}>
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
                href={project.github}
                >View Project
              </Button>
            </div>
          </Accordion.Content>
        </Accordion.Item>
      {/each}
    </Accordion.Root>
  </div>
</section>
