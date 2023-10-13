<script>
  import "../app.css";
  import Header from "../components/Header.svelte";
  import Footer from "../components/Footer.svelte";
  import PreFooter from "../components/PreFooter.svelte";

  let y;
  let innerWidth = 0;
  let innerHeight = 0;

  function goTop() {
    document.body.scrollIntoView({ behavior: "smooth" });
  }
</script>

<div
  class="relative flex flex-col max-w-[1400px] mx-auto w-full text-sm sm:text-base min-h-screen"
>
  <Header {y} />
  <slot />
</div>
<PreFooter />
<Footer />

<svelte:window bind:scrollY={y} bind:innerHeight bind:innerWidth />
