<script lang="ts">
  export let hasDownloadButton = false;
</script>

<footer class:center={!hasDownloadButton}>
  <div class="policy-container">
    <div class="links">
      <a href="/privacy-policy">Privacy Policy</a>
      <a href="/terms-of-use">Term of Use</a>
      <a href="/eula">E.U.L.A</a>
    </div>

    <div class="copyright-text">Copyright &copy; 2023 WanLog. All Rights Reserved.</div>
  </div>

  {#if hasDownloadButton}
    <button class="appstore-button" type="button">
      <img src="/images/appstore.png" alt="Download on the App Store" />
    </button>
  {/if}
</footer>

<style>
  footer {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 48px;
  }

  .center {
    justify-content: center;
  }

  .center > .policy-container {
    display: inline-flex;
    flex-direction: column;
    align-items: center;
  }

  .appstore-button {
    border: 1px solid white;
    background-color: black;
    border-radius: 6px;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    padding: 4px 12px;
  }

  .appstore-button:hover img {
    scale: 1.1;
  }

  .appstore-button > img {
    height: 48px;
    transition: scale 200ms;
  }

  .copyright-text {
    margin-top: 16px;
    font-size: 14px;
    color: #9e9e9e;
  }

  .links > a {
    font-size: 14px;
  }

  .links > a + a {
    margin-left: 8px;
  }
</style>
