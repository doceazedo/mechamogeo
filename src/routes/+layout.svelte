<script lang="ts">
  import '$lib/sass/minireset.sass';
  import '$lib/sass/global.sass';
  import { Navbar } from '$lib/components/navbar';
  import { Hero } from '$lib/components/hero';
</script>

<div class="container">
  <Navbar />
  <aside class="info">
    <Hero />
  </aside>
  <main class="page-content">
    <slot />
  </main>
</div>

<style lang="sass">
  .container
    display: flex
    gap: 4rem

  .info,
  .page-content
    width: 50%
    flex-grow: 1
    padding: 4rem 0
</style>
