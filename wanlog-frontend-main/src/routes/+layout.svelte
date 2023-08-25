<script lang="ts">
  import "$lib/styles/reset.css";
  import "$lib/styles/main.css";
</script>

<img src="/images/logo.png" alt="Logo" class="background-logo" />
<slot />

<style>
  .background-logo {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    opacity: 0.2;
    z-index: -1;
  }
</style>
