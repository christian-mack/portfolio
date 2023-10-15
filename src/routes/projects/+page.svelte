<script>
  import { Button } from "$components/ui/button";
  let projects = [];
</script>

<section>
  <h1 class="text-9xl text-center my-20">
    What I've been <span class="text-green-500">working on</span> so far
  </h1>
  <div class="w-full">
    <div class="flex">
      <div class="w-2/4">
        <div class="bg-slate-600 rounded-2xl">
          <img
            src="https://picsum.photos/500/400"
            alt="random"
            class="mx-auto"
          />
        </div>
        <div class="flex justify-between my-8">
          <div>
            <p>Estatery</p>
            <p>UIUX</p>
          </div>
          <Button>View</Button>
        </div>
      </div>

      <div class="w-2/4">
        <div class="bg-slate-600 rounded-2xl">
          <img
            src="https://picsum.photos/500/400"
            alt="random"
            class="mx-auto"
          />
        </div>
        <div class="flex justify-between my-8">
          <div>
            <p>Estatery</p>
            <p>UIUX</p>
          </div>
          <Button>View</Button>
        </div>
      </div>
    </div>

    <div class="w-full">
      <div
        class="bg-slate-600 rounded-2xl items-center justify-center overflow-hidden"
      >
        <img
          src="https://picsum.photos/1000/550"
          alt="random"
          class="mx-auto"
        />
      </div>
      <div class="flex justify-between my-8">
        <div>
          <p>Estatery</p>
          <p>UIUX</p>
        </div>
        <Button>View</Button>
      </div>
    </div>
  </div>
</section>
