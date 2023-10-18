<script>
  import { Button } from "$components/ui/button";
</script>

<section class="w-full">
  <div class="text-center items-center justify-center mx-52">
    <h1 class="text-8xl mt-10 mb-6 font-bold">
      <span class="text-green-500">Say Hi!</span> and tell me about your idea
    </h1>
    <p class="text-3xl font-light text-green-400">
      Have a nice idea? Reach out and let's chat.
    </p>
    <div id="formWrapper" class="flex flex-col">
      <form method="POST">
        <label for="name">Name</label>
        <input type="text" id="name" />

        <Button variant="ghostGreen" type="submit">Submit</Button>
      </form>
    </div>
  </div>
</section>
