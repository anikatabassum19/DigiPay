<script>
  // @ts-nocheck

  import {
    Navbar,
    NavBrand,
    NavLi,
    NavUl,
    NavHamburger,
    Dropdown,
    DropdownItem,
    DropdownDivider,
  } from "flowbite-svelte";
  import { ChevronDownOutline } from "flowbite-svelte-icons";
  import { page } from "$app/stores";
  $: activeUrl = $page.url.pathname;

  let dropVisibility = false;
  let ToolsVar = false;
  let AccVar = false;

  function FinanceDrop() {
    setTimeout(() => {
      dropVisibility = !dropVisibility;
      ToolsVar = false;
      AccVar = false;
    }, 100);
  }

  function ToolsDrop() {
    setTimeout(() => {
      ToolsVar = !ToolsVar;
      dropVisibility = false;
      AccVar = false;
    }, 100);
  }

  function AccDrop() {
    setTimeout(() => {
      AccVar = !AccVar;
      dropVisibility = false;
      ToolsVar = false;
    }, 100);
  }
</script>

<div class="w-full sticky inset-0 z-[100] flex justify-center bg-[#080312]">
  <nav
    class=" w-2/3 flex justify-between relative z-[100] items-center text-white p-5"
    style="font-family: 'Montserrat', sans-serif;"
  >
    <div class="flex space-x-10 w-fit">
      <a href="/" class="w-fit">
        <img src="../src/images/ratio2.png" alt="" class="w-1/3" />
      </a>
    </div>

    <!-- svelte-ignore missing-declaration -->
    <ul
      class="text-white flex items-center space-x-10"
      style="font-family: 'Montserrat', sans-serif;"
    >
      <li>
        <h1 class="text-white text-xs">Home</h1>
      </li>

      <!-- svelte-ignore a11y-click-events-have-key-events -->
      <!-- svelte-ignore a11y-no-noninteractive-element-interactions -->
      <li class="cursor-pointer" on:click={FinanceDrop}>
        <div class=" flex items-center hover:text-yellow-300">
          <h1
            class="text-white text-xs hover:text-yellow-300 hover:font-semibold transition-all"
          >
            Finance
          </h1>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="w-4 h-4"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="m19.5 8.25-7.5 7.5-7.5-7.5"
            />
          </svg>
        </div>

        {#if dropVisibility}
          <div
            class="absolute w-32 flex flex-col pl-2 p-2 rounded-xl shadow-xl space-y-2 mt-4 bg-white text-black text-xs"
          >
            <!-- svelte-ignore a11y-invalid-attribute -->
            <a href="">Transaction</a>
            <!-- svelte-ignore a11y-invalid-attribute -->
            <a href="">Wallet</a>
            <!-- svelte-ignore a11y-invalid-attribute -->
            <a href="">Market</a>
            <!-- svelte-ignore a11y-invalid-attribute -->
            <a href="">Exchange</a>
          </div>
        {/if}
      </li>

      <!-- svelte-ignore missing-declaration -->
      <!-- svelte-ignore a11y-click-events-have-key-events -->
      <!-- svelte-ignore a11y-no-noninteractive-element-interactions -->
      <li class="cursor-pointer" on:click={ToolsDrop}>
        <div class=" flex items-center hover:text-yellow-300">
          <h1
            class="text-white text-xs hover:text-yellow-300 hover:font-semibold transition-all"
          >
            Tools
          </h1>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="w-4 h-4"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="m19.5 8.25-7.5 7.5-7.5-7.5"
            />
          </svg>
        </div>

        {#if ToolsVar}
          <div
            class="absolute w-32 flex flex-col pl-2 p-2 rounded-xl shadow-xl space-y-2 mt-4 bg-white text-black text-xs"
          >
            <!-- svelte-ignore a11y-invalid-attribute -->
            <a href="">unit Converter</a>
            <!-- svelte-ignore a11y-invalid-attribute -->
            <a href="">CSV Export</a>
          </div>
        {/if}
      </li>

      <!-- svelte-ignore missing-declaration -->
      <!-- svelte-ignore a11y-click-events-have-key-events -->
      <!-- svelte-ignore a11y-no-noninteractive-element-interactions -->
      <li class="cursor-pointer" on:click={AccDrop}>
        <div class=" flex items-center hover:text-yellow-300">
          <h1
            class="text-white text-xs hover:text-yellow-300 hover:font-semibold transition-all"
          >
            Account
          </h1>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="w-4 h-4"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="m19.5 8.25-7.5 7.5-7.5-7.5"
            />
          </svg>
        </div>

        {#if AccVar}
          <!-- svelte-ignore a11y-invalid-attribute -->
          <div
            class="absolute w-32 flex flex-col pl-2 p-2 rounded-xl shadow-xl space-y-2 mt-4 bg-white text-black text-xs"
          >
            <!-- svelte-ignore a11y-invalid-attribute -->
            <a href="">Profile</a>
            <!-- svelte-ignore a11y-invalid-attribute -->
            <a href="">Login/Register</a>

            <!-- svelte-ignore a11y-invalid-attribute -->
            <a href="">Account Balance Checker</a>
            <!-- svelte-ignore a11y-invalid-attribute -->
            <!-- svelte-ignore a11y-invalid-attribute -->
            <a href="">Dex Tracker</a>
            <a href="">Node Tracker</a>
            <a href="">Label Cloud</a>
          </div>
        {/if}
      </li>

      <li>
        <button class="logbtn text-xs">Login </button>
      </li>
    </ul>
  </nav>
</div>

<style>
  .logbtn {
    border-radius: 0.25rem;
    text-transform: uppercase;
    font-style: normal;
    font-weight: 400;
    padding-left: 25px;
    padding-right: 25px;
    color: #fff;
    -webkit-clip-path: polygon(
      0 0,
      0 0,
      100% 0,
      100% 0,
      100% calc(100% - 15px),
      calc(100% - 15px) 100%,
      15px 100%,
      0 100%
    );
    clip-path: polygon(
      0 0,
      0 0,
      100% 0,
      100% 0,
      100% calc(100% - 15px),
      calc(100% - 15px) 100%,
      15px 100%,
      0 100%
    );
    height: 40px;
    font-size: 0.7rem;
    line-height: 14px;
    letter-spacing: 1.2px;
    transition: 0.2s 0.1s;
    background-image: linear-gradient(-45deg, #ff4040, #1c2bff);
    border: 0 solid;
    overflow: hidden;
  }

  .logbtn:hover {
    cursor: pointer;
    transition: all 0.3s ease-in;
    padding-right: 30px;
    padding-left: 30px;
  }
</style>
