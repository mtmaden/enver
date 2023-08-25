<script>
  import Footer from "$lib/components/organism/Footer.svelte";
  import Header from "$lib/components/organism/Header.svelte";
  import { Splide, SplideSlide } from "@splidejs/svelte-splide";
  import "@splidejs/svelte-splide/css";
  import "@splidejs/svelte-splide/css/core";
</script>

<div class="container">
  <Header>
    <button class="unlist-button">Unlist</button>
  </Header>

  <main>
    <div class="phone">
      <img src="/images/iphone-mockup.png" alt="iPhone Mockup" />
      <div class="slider">
        <Splide
          options={{
            width: 269,
            type: "loop",
            autoplay: true,
            arrows: false
          }}
        >
          <SplideSlide>
            <img src="/images/page-0.jpg" alt="Detail Page" />
          </SplideSlide>
          <SplideSlide>
            <img src="/images/page-1.jpg" alt="Detail Page" />
          </SplideSlide>
          <SplideSlide>
            <img src="/images/page-2.jpg" alt="Detail Page" />
          </SplideSlide>
          <SplideSlide>
            <img src="/images/page-3.jpg" alt="Detail Page" />
          </SplideSlide>
          <SplideSlide>
            <img src="/images/page-4.jpg" alt="Detail Page" />
          </SplideSlide>
          <SplideSlide>
            <img src="/images/page-5.jpg" alt="Detail Page" />
          </SplideSlide>
        </Splide>
      </div>
    </div>
  </main>

  <Footer hasDownloadButton />
</div>

<style>
  .container {
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    position: relative;
  }

  main {
    flex: 1;
    display: flex;
    align-items: center;

    justify-content: center;
  }

  .phone {
    width: 269px;
    height: 553px;
    position: relative;
    z-index: 1;
  }

  .phone > img {
    position: absolute;
    inset: 0;
    width: 100%;
    height: 100%;
    user-select: none;
    pointer-events: none;
  }

  .slider {
    width: 248px;
    height: 530px;
    border-radius: 30px;
    overflow: hidden;
    position: absolute;
    left: 50%;
    top: 50%;
    z-index: -1;
    transform: translate(-50%, -50%);
  }

  .slider img {
    width: 100%;
    height: 100%;
  }

  .unlist-button {
    appearance: none;
    border: 0;
    background-color: #673ab7;
    font-size: 1.2rem;
    padding: 1rem 2rem;
    border-radius: 6px;
    color: #fff;
    transition: background-color 200ms;
    cursor: pointer;
    font-weight: 500;
  }

  .unlist-button:hover {
    background-color: #5c6bc0;
  }
</style>
