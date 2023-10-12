<script lang="ts">
  export let y;

  const tabs = [
    { name: "About", href: "#about" },
    { name: "Projects", href: "#projects" },
    { name: "Contact", href: "#contact" },
  ];
</script>

<header
  class={"top-0 duration-200 px-6 flex items-center justify-between " +
    (y > 0 ? " py-4 bg-slate-950" : " py-6 bg-transparent border-transparent")}
>
  <h1 class="font-medium">
    <b class="font-bold poppins">Christian</b> Mack
  </h1>
  <div class="sm:flex items-center gap-4 hidden">
    {#each tabs as tab, index}
      <a href={tab.href} class="duration-200 hover:text-violet-400">
        <p>{tab.name}</p>
      </a>
    {/each}

    <a
      href="https://www.linkedin.com/in/christianmack2023"
      target="_blank"
      class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-white text-slate-950"
    >
      <h4 class="relative z-9">Get in touch</h4>
    </a>
  </div>
</header>
