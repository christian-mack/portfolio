<script>
  import { Button } from "$components/ui/button";
  import * as Accordion from "$components/ui/accordion";
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
      <Accordion.Item value="project-1">
        <Accordion.Trigger class="text-2xl mt-4 pb-10 hover:no-underline"
          ><div class="flex w-full justify-between">
            <h1>Web Scraper</h1>
            <p>
              Description for the project that is about this long. Perhaps a
              little bit longer. Such
            </p>
            <div>
              <Button variant="ghost">Tech</Button>
              <Button variant="ghost">Tech</Button>
            </div>
          </div></Accordion.Trigger
        >
        <Accordion.Content class="pb-4">
          Yes. It adheres to the WAI-ARIA design pattern.
        </Accordion.Content>
      </Accordion.Item>
      <Accordion.Item value="project-2">
        <Accordion.Trigger class="text-2xl pb-10 mt-4 hover:no-underline"
          ><div class="flex w-full justify-between">
            <h1>AI SEO Assistant</h1>
            <p>
              Description for the project that is about this long. Perhaps a
              little bit longer. Such
            </p>
            <div>
              <Button variant="ghost">Tech</Button>
              <Button variant="ghost">Tech</Button>
            </div>
          </div></Accordion.Trigger
        >
        <Accordion.Content class="pb-4">
          Yes. It adheres to the WAI-ARIA design pattern.
        </Accordion.Content>
      </Accordion.Item>
      <Accordion.Item value="project-3">
        <Accordion.Trigger class="text-2xl pb-10 mt-4 hover:no-underline"
          ><div class="flex w-full justify-between">
            <h3>Portfolio</h3>
            <p>
              Description for the project that is about this long. Perhaps a
              little bit longer. Such
            </p>
            <div>
              <Button variant="ghost">Tech</Button>
              <Button variant="ghost">Tech</Button>
            </div>
          </div></Accordion.Trigger
        >
        <Accordion.Content class="pb-4">
          Yes. It adheres to the WAI-ARIA design pattern.
        </Accordion.Content>
      </Accordion.Item>
    </Accordion.Root>
  </div>
</section>
