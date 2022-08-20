<script lang="ts">
  const pages = [
    {
      label: 'Início',
      href: '/',
    },
    {
      label: 'Sobre mim',
      href: '/about',
    },
    {
      label: 'Contato',
      href: '/contact',
    },
  ];
</script>

<nav>
  <ul>
    {#each pages as page, i}
      <li>
        <a href={page.href}>0{i + 1}. {page.label}</a>
      </li>
    {/each}
  </ul>
</nav>

<style lang="sass">
  nav
    width: 4rem
    height: 100%
    padding: 4rem 0
    background-color: #fff
    writing-mode: vertical-rl
    text-orientation: mixed
    font-size: 1.25rem

    ul
      display: flex
      gap: 1.5rem
      width: 100%

      li
        display: flex
        align-items: center

        a
          color: #000
          text-decoration: none
</style>
