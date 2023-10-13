<script>
  import { Button } from "$components/ui/button";

  let benefits = [
    {
      name: "a self-taught developer",
      description:
        "I am a full stack developer with a passion for building beautiful, functional, and responsive web applications.",
      icon: "fa-solid fa-laptop-code",
    },
    {
      name: "a problem solver",
      description:
        "I love solving problems and learning new things. I am always looking for ways to improve my skills and knowledge.",
      icon: "fa-solid fa-lightbulb-on",
    },
    {
      name: "a team player",
      description:
        "I am a team player who is always willing to help others and work together to achieve a common goal.",
      icon: "fa-solid fa-users",
    },
    {
      name: "a lifelong learner",
      description:
        "I am a lifelong learner who is always looking for ways to improve my skills and knowledge.",
      icon: "fa-solid fa-book",
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
</section>
