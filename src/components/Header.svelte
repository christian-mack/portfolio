<script>
  import { Button } from "$components/ui/button";
  import { Menu, Linkedin, Github, Instagram } from "lucide-svelte";
  import * as Sheet from "$components/ui/sheet";

  export let y;

  const tabs = [
    { name: "Home", href: "/" },
    { name: "About", href: "/about" },
    { name: "Projects", href: "/projects" },
  ];

  let showMenu = false;
  const handleTabClick = () => {
    showMenu = !showMenu;
  };
</script>

<header
  class={"top-0 duration-200 flex items-center justify-between px-4 " +
    (y > 0 ? "py-4 bg-slate-950" : "py-6 bg-transparent border-transparent")}
>
  <a href="/" class="cursor-pointer">
    <h1 class="poppins text-2xl">
      <b class="font-bold text-green-500">christian</b>mack
    </h1>
  </a>
  <div class="sm:flex items-center gap-4">
    <Button
      href="mailto:christian.ak.mack@gmail.com"
      target="_blank"
      variant="ghostGreen"
      class="hidden sm:flex p-6 lg:p-8">Get in touch &rarr;</Button
    >
    <Sheet.Root class="text-slate-100 border-none" bind:open={showMenu}>
      <Sheet.Trigger>
        <Button variant="ghostGreen" class="p-6 lg:p-8"><Menu /></Button>
      </Sheet.Trigger>
      <Sheet.Content
        side="top"
        class="flex bg-slate-950 text-slate-100 w-full items-center justify-center"
      >
        <div class="flex items-center w-full max-w-6xl">
          <Sheet.Header class="w-full">
            <Sheet.Title class="text-slate-400"
              >Are you looking for my resume? <Button
                variant="ghostGreenSolid"
                href="./christian-mack-resume.pdf"
                class="p-4 font-semibold cursor-pointer">Download here</Button
              ></Sheet.Title
            >
            <Sheet.Description
              class="w-full flex flex-col border-t-2 border-b-2 border-slate-700 pt-8 pb-9 gap-6"
            >
              {#each tabs as tab, index}
                <a
                  href={tab.href}
                  class="duration-200 text-slate-200 hover:text-green-500"
                  on:click={() => handleTabClick()}
                >
                  <p class="text-6xl lg:text-8xl text-start">{tab.name}</p>
                </a>
              {/each}
            </Sheet.Description>
            <Sheet.Footer
              class="flex flex-col md:flex-row justify-between text-slate-950 py-8 w-full"
            >
              <div class="w-full">
                <p class="text-slate-500 text-2xl font-medium">Follow Me.</p>
                <div
                  class="flex w-full lg:w-fit mt-6 justify-between md:justify-start"
                >
                  <Button
                    variant="link"
                    href="https://www.linkedin.com/in/christianmack2023/"
                    class="text-slate-300 hover:text-green-500 "
                  >
                    <Linkedin size={40} />
                  </Button>
                  <Button
                    variant="link"
                    href="https://github.com/christian-mack"
                    class="text-slate-300 hover:text-green-500"
                    ><Github size={40} /></Button
                  >
                  <Button
                    variant="link"
                    href="https://www.instagram.com/thechristianmack"
                    class="text-slate-300 hover:text-green-500"
                    ><Instagram size={40} /></Button
                  >
                </div>
              </div>
              <div class="w-full md:flex flex-col">
                <p class="text-slate-500 text-2xl font-medium pt-8 md:pt-0">
                  Stay connected with me.
                </p>
                <div
                  class="flex w-full lg:w-fit mt-6 justify-center md:justify-between"
                >
                  <Button
                    variant="ghostGreen"
                    href="mailto:christian.ak.mack@gmail.com"
                    class="p-8">Send me an email</Button
                  >
                </div>
              </div></Sheet.Footer
            >
          </Sheet.Header>
        </div>
      </Sheet.Content>
    </Sheet.Root>
  </div>
</header>
