<script lang="ts">
  import { GithubIcon, TwitterIcon } from 'svelte-feather-icons';

  const socials = [
    {
      icon: GithubIcon,
      href: 'https://github.com/mechamogeo',
      label: 'GitHub',
    },
    {
      icon: TwitterIcon,
      href: 'https://twitter.com/mechamogeo',
      label: 'Twitter',
    },
  ];
</script>

<div class="hero">
  <h1>Oi, eu me<br />chamo Geo.</h1>
  <p>
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Neque, ad non.
    Perspiciatis eligendi voluptatibus soluta praesentium, voluptas asperiores
    perferendis deserunt quae rem dolores placeat. Ratione magni ut assumenda
    ea. Aspernatur?
  </p>
  <div class="socials">
    {#each socials as social}
      <a href={social.href}>
        <svelte:component this={social.icon} size="16" />
        {social.label}
      </a>
    {/each}
  </div>
  <img src="/geo.jpg" alt="" />
</div>

<style lang="sass">
  .hero
    display: flex
    flex-direction: column
    gap: 4rem

  h1
    font-size: 4rem
    font-weight: 700
    line-height: 1

  p
    color: rgba(#fff, .75)
    font-size: 1.25rem
    line-height: 1.5

  .socials
    display: flex
    gap: 2rem
    line-height: 1.5

    a
      display: flex
      align-items: center
      gap: .5rem
      color: rgba(#fff, .75)
      text-decoration: none

  img
    position: absolute
    left: 2rem
    bottom: 4rem
</style>
