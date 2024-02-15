<script>
  let dropDownOn = false;

  function toggleoptionButton() {
    dropDownOn = !dropDownOn;
    console.log("dropDownOn:", dropDownOn);
  }
  let firstTxt;

  let windowHeigh = 0;
  let scrollPosition = 0;
  let rootEl = 0;
  let text =
    "DIGIPAY<< DECENTRALIZED MONEY TRANSFER SYSTEM DIGIPAY DECENTRALIZED MONEY TRANSFER SYSTEM DIGIPAY<< DECENTRALIZED MONEY TRANSFER SYSTEM DIGIPAY DECENTRALIZED MONEY TRANSFER SYSTEM ";

  function scrollMove() {
    let deltaScrollPos =
      // @ts-ignore
      Math.abs(rootEl.getBoundingClientRect().top - windowHeigh) /
      // @ts-ignore
      rootEl.clientHeight;

    // @ts-ignore
    firstTxt.style.transform = `translateX(${deltaScrollPos * -500}px)`;
  }
</script>

<svelte:window
  bind:innerHeight={windowHeigh}
  on:scroll={scrollMove}
  bind:scrollY={scrollPosition}
/>

<section
  class="text-white overflow-hidden"
  bind:this={rootEl}
  style="font-family: 'Montserrat', serif;"
>
  <div class="w-full h-full">
    <div class="absolute w-full h-[50rem] bg-gradient-to-l fadedbg"></div>

    <div class=" mt-20">
      <div class="w-full p-2 grid justify-center">
        <div class="grid justify-center">
          <div class="">
            <img
              src="../src/images/blob3.png"
              alt=""
              class="absolute blur-[90px] -z-50 opacity-50 w-1/5 translate-x-[23rem] mix-blend-screen"
            />
          </div>
          <div
            class="grid items-center w-full justify-center text-center mx-auto"
          >
            <div class="flex text-center">
              <h1
                class="text-4xl font-semibold"
                style="font-family: 'Montserrat', serif;"
              >
                Securing Your
              </h1>
              <h1
                class="text-4xl bg-gradient-to-r from-[#7e03aa] to-[#00fffb] bg-clip-text text-transparent font-bold"
                style="font-family: 'Montserrat', serif;"
              >
                &nbsp;Finances,
              </h1>
              <h1
                class="text-4xl font-semibold"
                style="font-family: 'Montserrat', serif;"
              >
                &nbsp;Unleashing
              </h1>
            </div>

            <h1
              class="text-4xl bg-gradient-to-r from-[#7e03aa] to-[#ffae00] bg-clip-text text-transparent font-bold"
              style="font-family: 'Montserrat', serif;"
            >
              &nbsp;Decentralized Possibilities
            </h1>
          </div>
        </div>

        <h5
          class="text-sm font-light flex justify-center mt-2"
          style="font-family: 'Montserrat', sans-serif;"
        >
          Web 3.0 Begins
        </h5>
        <div class="flex 2-full justify-center">
          <button class="btn mt-5 w-1/2 h-[4rem]"> Connect Wallet </button>
        </div>
      </div>

      <div class="flex justify-center fadedbg">
        <div class="w-fit flex justify-center -z-50 -translate-y-28">
          <img
            src="../src/images/bgdes1.png"
            alt=""
            class="aspect-square object-cover w-1/2"
          />
        </div>

        <div class="">
          <img
            src="../src/images/blob3.png"
            alt=""
            class="absolute inset-0 blur-[90px] -z-50 opacity-100 w-1/3 translate-y-[38rem] translate-x-[23rem] mix-blend-color-dodge"
          />
        </div>
      </div>

      <div class="w-full flex justify-center -translate-y-44">
        <div
          class="w-full flex justify-center border-t border-b border-[#4435556e]"
        >
          <h1
            style="font-family: 'Montserrat', serif;"
            class="font-black text-[#4435556e] text-[3rem] w-full whitespace-nowrap"
            bind:this={firstTxt}
          >
            {text}
          </h1>
        </div>
      </div>

      <div class="w-full flex justify-center">
        <div
          class="w-1/2 flex items-center justify-center p-3 rounded-3xl bg-black"
        >
          <div>
            <img
              src="../src/images/ETH.png"
              alt=""
              class="aspect-square object-cover w-[23rem]"
            />
          </div>
          <div class="form-container w-fit h-fit">
            <h1 class="text-xl font-bold">Connect Your Wallet</h1>
            <form class="form">
              <div class="form-group">
                <label for="email">Address To</label>
                <input type="text" id="email" name="email" required />
              </div>

              <div class="form-group">
                <label for="email">Ammount (ETH)</label>
                <input type="text" id="email" name="email" required />
              </div>

              <div class="form-group">
                <label for="email">Keyword</label>
                <input type="text" id="email" name="email" required />
              </div>

              <div class="form-group">
                <label for="textarea">Enter Message</label>
                <textarea name="textarea" id="textarea" rows="10" cols="50"
                ></textarea>
              </div>

              <button class="form-submit-btn" type="submit"
                >Connect Wallet</button
              >
            </form>
          </div>
        </div>
      </div>
      <!-- Lower part -->

      <div class="flex justify-center space-x-20">
        <div class="w-1/3 flex bg-black p-5 mt-10 mb-10 rounded-xl">
          <div class="">
            <div class="card">
              <svg
                class="img"
                xmlns="http://www.w3.org/2000/svg"
                xml:space="preserve"
                width="100%"
                height="100%"
                version="1.1"
                shape-rendering="geometricPrecision"
                text-rendering="geometricPrecision"
                image-rendering="optimizeQuality"
                fill-rule="evenodd"
                clip-rule="evenodd"
                viewBox="0 0 784.37 1277.39"
                xmlns:xlink="http://www.w3.org/1999/xlink"
              >
                <g id="Layer_x0020_1">
                  <metadata id="CorelCorpID_0Corel-Layer"></metadata>
                  <g id="_1421394342400">
                    <g>
                      <polygon
                        fill="#343434"
                        fill-rule="nonzero"
                        points="392.07,0 383.5,29.11 383.5,873.74 392.07,882.29 784.13,650.54"
                      ></polygon>
                      <polygon
                        fill="#8C8C8C"
                        fill-rule="nonzero"
                        points="392.07,0 -0,650.54 392.07,882.29 392.07,472.33"
                      ></polygon>
                      <polygon
                        fill="#3C3C3B"
                        fill-rule="nonzero"
                        points="392.07,956.52 387.24,962.41 387.24,1263.28 392.07,1277.38 784.37,724.89"
                      ></polygon>
                      <polygon
                        fill="#8C8C8C"
                        fill-rule="nonzero"
                        points="392.07,1277.38 392.07,956.52 -0,724.89"
                      ></polygon>
                      <polygon
                        fill="#141414"
                        fill-rule="nonzero"
                        points="392.07,882.29 784.13,650.54 392.07,472.33"
                      ></polygon>
                      <polygon
                        fill="#393939"
                        fill-rule="nonzero"
                        points="0,650.54 392.07,882.29 392.07,472.33"
                      ></polygon>
                    </g>
                  </g>
                </g>
              </svg>
              <div class="textBox">
                <p class="text head">Ethereum</p>
                <span>Cryptocurrency</span>
                <p class="text price">$24746188474.31</p>
              </div>
            </div>
          </div>

          <div class="flex w-1/2 items-center">
            <div
              class=" space-y-5 ml-20 flex flex-col align-middle"
              style="font-family: 'Montserrat', sans-serif;
                "
            >
              <h1
                class="text-white text-2xl font-semibold uppercase"
                style="font-family: 'Montserrat', sans-serif;
                  "
              >
                Etherium
              </h1>
              <h1
                class="text-sm w-full"
                style="font-family: 'Montserrat', sans-serif;
                  "
              >
                The live Ethereum price today is $2548.56 USD with a 24-hour
                trading volume of $24746188474.31 USD.
              </h1>

              <div class=" relative inline-flex">
                <button
                  type="button"
                  on:click={toggleoptionButton}
                  class=" py-3 px-4 inline-flex items-center gap-x-2 text-sm font-medium rounded-lg text-white bg-[#FF9119]
                        disabled:opacity-50 disabled:pointer-events-none dark:border-gray-700 dark:focus:ring-1"
                >
                  Select Coin
                  <svg
                    class="hs-dropdown-open:rotate-180 w-4 h-4"
                    xmlns="http://www.w3.org/2000/svg"
                    width="24"
                    height="24"
                    viewBox="0 0 24 24"
                    fill="none"
                    stroke="currentColor"
                    stroke-width="2"
                    stroke-linecap="round"
                    stroke-linejoin="round"><path d="m6 9 6 6 6-6" /></svg
                  >
                </button>

                {#if dropDownOn}
                  <div
                    class="absolute z-50 shadow-xl transition-[opacity,margin] duration hs-dropdown-open:opacity-100 min-w-[15rem] bg-white rounded-lg p-2 mt-16 divide-y divide-gray-200 dark:bg-gray-800 dark:border dark:border-gray-700 dark:divide-gray-700"
                    aria-labelledby="hs-dropdown-with-icons"
                  >
                    <div class="py-2 first:pt-0 last:pb-0">
                      <a
                        class="flex items-center gap-x-3.5 py-2 px-3 rounded-lg text-sm text-gray-800 hover:bg-gray-100 focus:outline-none focus:bg-gray-100 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-gray-300 dark:focus:bg-gray-700"
                        href="#"
                      >
                        <svg
                          class="flex-shrink-0 w-4 h-4"
                          xmlns="http://www.w3.org/2000/svg"
                          width="24"
                          height="24"
                          viewBox="0 0 24 24"
                          fill="none"
                          stroke="currentColor"
                          stroke-width="2"
                          stroke-linecap="round"
                          stroke-linejoin="round"
                          ><path
                            d="M6 8a6 6 0 0 1 12 0c0 7 3 9 3 9H3s3-2 3-9"
                          /><path d="M10.3 21a1.94 1.94 0 0 0 3.4 0" /></svg
                        >
                        Etherium
                      </a>
                      <a
                        class="flex items-center gap-x-3.5 py-2 px-3 rounded-lg text-sm text-gray-800 hover:bg-gray-100 focus:outline-none focus:bg-gray-100 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-gray-300 dark:focus:bg-gray-700"
                        href="#"
                      >
                        <svg
                          class="flex-shrink-0 w-4 h-4"
                          xmlns="http://www.w3.org/2000/svg"
                          width="24"
                          height="24"
                          viewBox="0 0 24 24"
                          fill="none"
                          stroke="currentColor"
                          stroke-width="2"
                          stroke-linecap="round"
                          stroke-linejoin="round"
                          ><circle cx="8" cy="21" r="1" /><circle
                            cx="19"
                            cy="21"
                            r="1"
                          /><path
                            d="M2.05 2.05h2l2.66 12.42a2 2 0 0 0 2 1.58h9.78a2 2 0 0 0 1.95-1.57l1.65-7.43H5.12"
                          /></svg
                        >
                        Bitcoin
                      </a>
                      <a
                        class="flex items-center gap-x-3.5 py-2 px-3 rounded-lg text-sm text-gray-800 hover:bg-gray-100 focus:outline-none focus:bg-gray-100 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-gray-300 dark:focus:bg-gray-700"
                        href="#"
                      >
                        <svg
                          class="flex-shrink-0 w-4 h-4"
                          xmlns="http://www.w3.org/2000/svg"
                          width="24"
                          height="24"
                          viewBox="0 0 24 24"
                          fill="none"
                          stroke="currentColor"
                          stroke-width="2"
                          stroke-linecap="round"
                          stroke-linejoin="round"
                          ><path
                            d="M4 14.899A7 7 0 1 1 15.71 8h1.79a4.5 4.5 0 0 1 2.5 8.242"
                          /><path d="M12 12v9" /><path d="m8 17 4 4 4-4" /></svg
                        >
                        Solana
                      </a>
                      <a
                        class="flex items-center gap-x-3.5 py-2 px-3 rounded-lg text-sm text-gray-800 hover:bg-gray-100 focus:outline-none focus:bg-gray-100 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-gray-300 dark:focus:bg-gray-700"
                        href="#"
                      >
                        <svg
                          class="flex-shrink-0 w-4 h-4"
                          xmlns="http://www.w3.org/2000/svg"
                          width="24"
                          height="24"
                          viewBox="0 0 24 24"
                          fill="none"
                          stroke="currentColor"
                          stroke-width="2"
                          stroke-linecap="round"
                          stroke-linejoin="round"
                          ><path
                            d="M16 21v-2a4 4 0 0 0-4-4H6a4 4 0 0 0-4 4v2"
                          /><circle cx="9" cy="7" r="4" /><path
                            d="M22 21v-2a4 4 0 0 0-3-3.87"
                          /><path d="M16 3.13a4 4 0 0 1 0 7.75" /></svg
                        >
                        Dot
                      </a>
                    </div>
                  </div>
                {/if}
              </div>
            </div>
          </div>
        </div>

        <!-- Converter -->

        <div>
          <div
            class="bg-black flex items-center p-5 mt-10 mb-10 space-x-10 rounded-xl"
          >
            <div class="">
              <img
                src="../src/images/convert.png"
                alt=""
                class=" aspect-square object-cover w-[20rem]"
              />
            </div>
            <div>
              <h1
                class="text-white text-xl font-semibold uppercase"
                style="font-family: 'Montserrat', sans-serif;
              "
              >
                Converter
              </h1>
              <h1
                class="text-sm"
                style="font-family: 'Montserrat', sans-serif;
              "
              >
                Enter the Amount and set the Unit to Convert
              </h1>

              <div class="mt-20 flex">
                <input
                  type="text"
                  class="bg-transparent outline-none text-white h-10 rounded-xl"
                />
                <button
                  type="button"
                  class=" ml-2 text-white w-1/2 justify-center bg-[#FF9119] hover:bg-[#FF9119]/80 focus:ring-4 focus:outline-none focus:ring-[#FF9119]/50 font-medium rounded-lg text-sm px-5 py-2.5 text-center inline-flex items-center dark:hover:bg-[#FF9119]/80 dark:focus:ring-[#FF9119]/40 me-2 mb-2"
                >
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke-width="1.5"
                    stroke="currentColor"
                    class="w-6 h-6"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M19.5 12c0-1.232-.046-2.453-.138-3.662a4.006 4.006 0 0 0-3.7-3.7 48.678 48.678 0 0 0-7.324 0 4.006 4.006 0 0 0-3.7 3.7c-.017.22-.032.441-.046.662M19.5 12l3-3m-3 3-3-3m-12 3c0 1.232.046 2.453.138 3.662a4.006 4.006 0 0 0 3.7 3.7 48.656 48.656 0 0 0 7.324 0 4.006 4.006 0 0 0 3.7-3.7c.017-.22.032-.441.046-.662M4.5 12l3 3m-3-3-3 3"
                    />
                  </svg>

                  convert
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div
        class="w-full flex justify-center mt-20 border-t border-slate-800 p-5"
      >
        <div>
          <h1 class="text-4xl font-bold text-slate-700">Some Common Queries</h1>
        </div>

        <div></div>
      </div>
    </div>
  </div>
</section>

<!-- from-[#2c2826] to-black -->

<style>
  .fadedbg {
    -webkit-mask-image: linear-gradient(#000, rgba(0, 0, 0, 0));
    mask-image: linear-gradient(#000, rgba(0, 0, 0, 0));
    z-index: -1;
  }

  /* ConnectBtn */

  .btn {
    --border-color: linear-gradient(-45deg, #ffae00, #7e03aa, #00fffb);
    --border-width: 0.125em;
    --curve-size: 0.5em;
    --blur: 30px;
    --bg: #080312;
    --color: #afffff;
    color: var(--color);
    /* use position: relative; so that BG is only for .btn */
    position: relative;
    isolation: isolate;
    display: inline-grid;
    place-content: center;
    padding: 0.5em 1.5em;
    font-size: 17px;
    border: 0;
    text-transform: uppercase;
    box-shadow: 10px 10px 20px rgba(0, 0, 0, 0.6);
    clip-path: polygon(
      /* Top-left */ 0% var(--curve-size),
      var(--curve-size) 0,
      /* top-right */ 100% 0,
      100% calc(100% - var(--curve-size)),
      calc(100% - var(--curve-size)) 100%,
      0 100%
    );
    transition: color 250ms;
  }

  .btn::after,
  .btn::before {
    content: "";
    position: absolute;
    inset: 0;
  }

  .btn::before {
    background: var(--border-color);
    background-size: 300% 300%;
    animation: move-bg7234 5s ease infinite;
    z-index: -2;
  }

  @keyframes move-bg7234 {
    0% {
      background-position: 31% 0%;
    }

    50% {
      background-position: 70% 100%;
    }

    100% {
      background-position: 31% 0%;
    }
  }

  .btn::after {
    background: var(--bg);
    z-index: -1;
    clip-path: polygon(
      /* Top-left */ var(--border-width)
        calc(var(--curve-size) + var(--border-width) * 0.5),
      calc(var(--curve-size) + var(--border-width) * 0.5) var(--border-width),
      /* top-right */ calc(100% - var(--border-width)) var(--border-width),
      calc(100% - var(--border-width))
        calc(100% - calc(var(--curve-size) + var(--border-width) * 0.5)),
      /* bottom-right 1 */
        calc(100% - calc(var(--curve-size) + var(--border-width) * 0.5))
        calc(100% - var(--border-width)),
      /* bottom-right 2 */ var(--border-width) calc(100% - var(--border-width))
    );
    transition: clip-path 500ms;
  }

  .btn:where(:hover, :focus)::after {
    clip-path: polygon(
      /* Top-left */ calc(100% - var(--border-width))
        calc(100% - calc(var(--curve-size) + var(--border-width) * 0.5)),
      calc(100% - var(--border-width)) var(--border-width),
      /* top-right */ calc(100% - var(--border-width)) var(--border-width),
      calc(100% - var(--border-width))
        calc(100% - calc(var(--curve-size) + var(--border-width) * 0.5)),
      /* bottom-right 1 */
        calc(100% - calc(var(--curve-size) + var(--border-width) * 0.5))
        calc(100% - var(--border-width)),
      /* bottom-right 2 */
        calc(100% - calc(var(--curve-size) + var(--border-width) * 0.5))
        calc(100% - var(--border-width))
    );
    transition: 200ms;
  }

  .btn:where(:hover, :focus) {
    color: #fff;
  }

  /* Form */

  .form-container {
    width: full;
    background:
      linear-gradient(#212121, #212121) padding-box,
      linear-gradient(145deg, transparent 35%, #e81cff, #40c9ff) border-box;
    border: 2px solid transparent;
    padding: 32px 24px;
    font-size: 12px;
    font-family: inherit;
    color: white;
    display: flex;
    flex-direction: column;
    gap: 10px;
    box-sizing: border-box;
    border-radius: 16px;
  }

  .form-container button:active {
    scale: 0.95;
  }

  .form-container .form {
    display: flex;
    flex-direction: column;
    gap: 20px;
  }

  .form-container .form-group {
    display: flex;
    flex-direction: column;
    gap: 2px;
  }

  .form-container .form-group label {
    display: block;
    margin-bottom: 5px;
    color: #717171;
    font-weight: 600;
    font-size: 12px;
  }

  .form-container .form-group input {
    width: 100%;
    padding: 5px;
    border-radius: 8px;
    color: #fff;
    font-family: inherit;
    background-color: transparent;
    border: 1px solid #414141;
  }

  .form-container .form-group textarea {
    width: 100%;
    padding: 5px;
    border-radius: 8px;
    resize: none;
    color: #fff;
    height: 96px;
    border: 1px solid #414141;
    background-color: transparent;
    font-family: inherit;
  }

  .form-container .form-group input::placeholder {
    opacity: 0.5;
  }

  .form-container .form-group input:focus {
    outline: none;
    border-color: #e81cff;
  }

  .form-container .form-group textarea:focus {
    outline: none;
    border-color: #e81cff;
  }

  .form-container .form-submit-btn {
    display: flex;
    align-items: flex-start;
    justify-content: center;
    align-self: flex-start;
    font-family: inherit;
    color: #717171;
    font-weight: 600;
    width: 40%;
    background: #313131;
    border: 1px solid #414141;
    padding: 12px 16px;
    font-size: inherit;
    gap: 8px;
    margin-top: 8px;
    cursor: pointer;
    border-radius: 6px;
  }

  .form-container .form-submit-btn:hover {
    background-color: #fff;
    border-color: #fff;
  }

  /* ETHERIUM CARD */
  .card {
    width: 195px;
    height: 285px;
    background: #080312;
    border-radius: 20px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    color: white;
    transition: 0.2s ease-in-out;
  }

  .img {
    color: #080312;
    width: fit-content;
    height: 30%;
    position: absolute;
    transition: 0.2s ease-in-out;
    z-index: 1;
  }

  .textBox {
    opacity: 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 15px;
    transition: 0.2s ease-in-out;
    z-index: 2;
  }

  .textBox > .text {
    font-weight: bold;
  }

  .textBox > .head {
    font-size: 20px;
  }

  .textBox > .price {
    font-size: 17px;
  }

  .textBox > span {
    font-size: 12px;
    color: lightgrey;
  }

  .card:hover > .textBox {
    opacity: 1;
  }

  .card:hover > .img {
    height: 65%;
    filter: blur(7px);
    animation: anim 3s infinite;
  }

  @keyframes anim {
    0% {
      transform: translateY(0);
    }

    50% {
      transform: translateY(-20px);
    }

    100% {
      transform: translateY(0);
    }
  }

  .card:hover {
    transform: scale(1.04) rotate(-1deg);
  }
</style>
