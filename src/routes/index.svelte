<script context="module">
  export const prerender = true;
</script>

<script>
  import Counter from "$lib/Counter.svelte";
</script>

<svelte:head>
  <title>Moving</title>
</svelte:head>

<section>
  <h1>
    <div class="welcome">
      <picture>
        <img src="doc.jpg" alt="Doc Brown" />
      </picture>
    </div>
  </h1>

  <h2>
    <strong>Be careful, </strong>for every click a baloon pops in a kid's hand
  </h2>

  <Counter />
</section>

<style>
  section {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    flex: 1;
  }

  h1 {
    width: 100%;
  }

  .welcome {
    position: relative;
    width: 100%;
    height: 0;
    padding: 0 0 calc(100% * 900 / 2048) 0;
  }

  .welcome img {
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    display: block;
  }
</style>
