<script>
  let dropDownOn = false;

  function toggleoptionButton() {
    dropDownOn = !dropDownOn;
    console.log("dropDownOn:", dropDownOn);
  }
</script>

<section class="text-white" style="font-family: 'Montserrat', serif;">
  <div class="w-full h-full object-cover">
    <div class="w-full">
      <div
        class="w-full h-[50rem] bg-gradient-to-l from-[#2c2826] to-black fadedbg"
      >
        <div>
          <img src="../src/images/bgdes1.png" alt="" class="  " />
        </div>
      </div>

      <div class="flex justify-start items-center absolute inset-0 mt-20">
        <div class="ml-40 z-50">
          <div class="w-full justify-center p-2">
            <h1
              class="text-4xl font-semibold"
              style="font-family: 'Montserrat', serif;"
            >
              Securing Your Finances, <br /> Unleashing Decentralized
              <br />Possibilities
            </h1>
            <h5
              class="text-sm font-light flex items-center mt-2"
              style="font-family: 'Montserrat', sans-serif;"
            >
              Web 3.0 Begins
            </h5>
            <button class="connectBtn"> Connect Wallet </button>
          </div>

          <div class="flex justify-center">
            <div class="form-container">
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
      </div>

      <div class="grid w-full justif-between mt-20">
        <div class="w-1/2 bg-black p-10 mt-40 mb-10 ml-10 rounded-xl">
          <div class="flex w-full items-center">
            <img src="../src/images/ETH.png" alt="" class="w-2/3" />
            <div
              class="card space-y-5 flex flex-col align-middle mr-10"
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

          <div class="card space-y-11">
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
                class="ml-2 text-white w-1/2 justify-center bg-[#FF9119] hover:bg-[#FF9119]/80 focus:ring-4 focus:outline-none focus:ring-[#FF9119]/50 font-medium rounded-lg text-sm px-5 py-2.5 text-center inline-flex items-center dark:hover:bg-[#FF9119]/80 dark:focus:ring-[#FF9119]/40 me-2 mb-2"
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
  </div>
</section>

<style>
  .fadedbg {
    -webkit-mask-image: linear-gradient(#000, rgba(0, 0, 0, 0));
    mask-image: linear-gradient(#000, rgba(0, 0, 0, 0));
    z-index: -1;
  }

  /* button code eta */

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

  /* Main Btn */
  .connectBtn {
    position: relative;
    padding: 10px 20px;
    border-radius: 7px;
    border: 1px solid #af7304;
    font-size: 10px;
    text-transform: uppercase;
    font-weight: 400;
    letter-spacing: 2px;
    background: transparent;
    color: #fff;
    overflow: hidden;
    box-shadow: 0 0 0 0 transparent;
    -webkit-transition: all 0.2s ease-in;
    -moz-transition: all 0.2s ease-in;
    transition: all 0.2s ease-in;
    width: 50%;
    height: 100%;
    margin-top: 20px;
  }

  .connectBtn:hover {
    background: #af7304;
    box-shadow: 0 0 30px 5px #af7304;
    -webkit-transition: all 0.2s ease-out;
    -moz-transition: all 0.2s ease-out;
    transition: all 0.2s ease-out;
  }

  .connectBtn:hover::before {
    -webkit-animation: sh02 0.5s 0s linear;
    -moz-animation: sh02 0.5s 0s linear;
    animation: sh02 0.5s 0s linear;
  }

  .connectBtn::before {
    content: "";
    display: block;
    width: 100%;
    height: 86%;
    position: absolute;
    top: 7%;
    left: 0%;
    opacity: 0;
    background: #fff;
    box-shadow: 0 0 50px 30px #fff;
    -webkit-transform: skewX(-20deg);
    -moz-transform: skewX(-20deg);
    -ms-transform: skewX(-20deg);
    -o-transform: skewX(-20deg);
    transform: skewX(-20deg);
  }

  @keyframes sh02 {
    from {
      opacity: 0;
      left: 0%;
    }

    50% {
      opacity: 1;
    }

    to {
      opacity: 0;
      left: 100%;
    }
  }

  .connectBtn:active {
    box-shadow: 0 0 0 0 transparent;
    -webkit-transition: box-shadow 0.2s ease-in;
    -moz-transition: box-shadow 0.2s ease-in;
    transition: box-shadow 0.2s ease-in;
  }
</style>
