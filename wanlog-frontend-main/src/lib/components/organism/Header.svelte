<header>
  <a href="/" aria-label="Homepage">
    <img src="/images/logo.png" alt="Logo" class="header-logo" />
  </a>

  <slot />
</header>

<style>
  header {
    padding: 4rem;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .header-logo {
    height: 6rem;
  }
</style>
