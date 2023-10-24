<script>
  import { Button } from "$components/ui/button";
  import * as Table from "$components/ui/table";
  import AboutImage from "$lib/assets/aboutplaceholder.jpeg";

  const experiences = [
    {
      title: "Full Stack Developer - Freelance",
      company: "Maverick Digital Solutions",
      dates: "Aug 2023 - Present",
    },
    {
      title: "Web Developer",
      company: "Prime Trust",
      dates: "Jul 2022 - Aug 2023",
    },
    {
      title: "Front-End Developer",
      company: "Foreign Languages for Kids",
      dates: "Jul 2021 - Jan 2022",
    },
  ];
</script>

<section id="about" class="py-12 px-4">
  <div><p class="text-xl font-medium mb-1 hidden md:flex">About Me</p></div>
  <div class="flex flex-col md:flex-row gap-5 md:gap-10">
    <h1 class="text-3xl md:text-6xl xl:text-8xl font-semibold">
      Passionate developer on a <span class="text-slate-400">mission</span>
    </h1>

    <div class="flex flex-col justify-between items-end">
      <p class="text-xl">
        I'm Christian, a Full Stack Developer roaming the globe, and I focus on
        developing digital experiences that are easy to use, enjoyable, and get
        the job done.
      </p>

      <Button
        href="mailto:christian.ak.mack@gmail.com"
        target="_blank"
        variant="ghostGreenSolid"
        class="w-fit text-base sm:text-lg md:text-xl relative rounded-full py-8 px-10 bg-green-600 text-slate-950 mt-7 md:mt-14"
        >Let's Talk &rarr;</Button
      >
    </div>
  </div>
  <div class="pt-12">
    <img src={AboutImage} alt="randomly generated" class="rounded-[24px]" />
  </div>
  <div class="mt-20">
    <h3 class="text-4xl md:text-5xl font-semibold mb-6 md:mb-12 text-green-500">
      My Experience
    </h3>
    <Table.Root>
      <Table.Header>
        <Table.Row />
      </Table.Header>
      <Table.Body>
        {#each experiences as experience}
          <Table.Row class="hover:bg-transparent">
            <Table.Cell
              class="font-medium flex w-full justify-between md:items-end py-8 px-0 flex-col md:flex-row md:gap-5"
            >
              <div class="flex flex-col">
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
