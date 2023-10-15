<script>
  import { Button } from "$components/ui/button";
  import * as Table from "$components/ui/table";
  import AboutImage from "$lib/assets/aboutplaceholder.jpeg";
  import ScrollText from "./ScrollText.svelte";

  const experiences = [
    {
      title: "Full Stack Developer",
      company: "Maverick Digital Solutions",
      dates: "2020 - 2021",
    },
    { title: "Web Developer", company: "Prime Trust", dates: "2021 - 2022" },
    {
      title: "Front-End Developer",
      company: "Foreign Languages for Kids",
      dates: "2022 - 2023",
    },
  ];
</script>

<section id="about" class="py-12">
  <div><p class="text-xl font-medium mb-1">About Me</p></div>
  <div class="flex">
    <h1 class="text-8xl font-semibold">
      Passionate developer on a <span class="text-slate-400">mission</span>
    </h1>

    <div class="flex flex-col justify-between items-end">
      <p class="text-xl">
        I'm Christian, a Full Stack Developer roaming the globe, and I focus on
        developing digital experiences that are easy to use, enjoyable, and get
        the job done.
      </p>

      <Button
        href="/contact"
        target="_blank"
        variant="ghost"
        class="w-fit text-base sm:text-lg md:text-xl relative rounded-full py-8 px-10 bg-green-600 text-slate-950 mt-14"
        >Let's Talk &rarr;</Button
      >
    </div>
  </div>
  <div class="py-12">
    <img src={AboutImage} alt="randomly generated" class="rounded-[24px]" />
  </div>
  <ScrollText />
  <div class="my-28">
    <h3 class="text-5xl font-semibold mb-12 text-green-400">My Experience</h3>
    <Table.Root>
      <!-- <Table.Caption>A list of your recent invoices.</Table.Caption> -->
      <Table.Header>
        <Table.Row />
      </Table.Header>
      <Table.Body>
        {#each experiences as experience}
          <Table.Row class="hover:bg-transparent">
            <Table.Cell
              class="font-medium flex w-full justify-between items-end py-8 px-0"
            >
              <div>
                <p class="mb-3 text-2xl font-medium">{experience.title}</p>
                <p class="text-lg font-light text-slate-300">
                  {experience.company}
                </p>
              </div>
              <p class="text-lg text-slate-300">
                {experience.dates}
              </p></Table.Cell
            >
          </Table.Row>
        {/each}
      </Table.Body>
    </Table.Root>
  </div>
</section>
