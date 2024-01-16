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
    
    <!-- <Navbar class="bg-[#353535] w-full text-white">
        <NavBrand href="/">
            <img
                src="../src/images/gray.png"
                class="me-3 h-6 aspect-square object-cover w-40 nm sm:h-9 "
                alt="DigiPay Logo"
            />
            <span
                class="self-center whitespace-nowrap text-xl font-semibold dark:text-white"
                >DigiPay</span
            >
        </NavBrand>
        
    
        <NavUl {activeUrl}>
            <NavLi href="/">Home</NavLi>
    
            <NavLi class="cursor-pointer">
                Finance<ChevronDownOutline
                    class="w-3 h-3 ms-2 text-primary-800 dark:text-white inline"
                />
            </NavLi>
            <Dropdown class="w-44 z-20">
                <DropdownItem href="/">Transactions</DropdownItem>
                <DropdownItem href="/">Wallet</DropdownItem>
                <DropdownItem href="/">Market</DropdownItem>
                <DropdownItem href="/">Exchange</DropdownItem>
                <DropdownItem href="/">Deposit/Withdraw Money</DropdownItem>
                <DropdownItem href="/">Blockchain Chat</DropdownItem>
            </Dropdown>
    
            <NavLi class="cursor-pointer">
                Tools<ChevronDownOutline
                    class="w-3 h-3 ms-2 text-primary-800 dark:text-white inline"
                />
            </NavLi>
            <Dropdown class="w-44 z-20">
                <DropdownItem href="/">Unit Converter</DropdownItem>
                <DropdownItem href="/">CSV Export</DropdownItem>
            </Dropdown>
    
            <NavLi class="cursor-pointer">
                Account<ChevronDownOutline
                    class="w-3 h-3 ms-2 text-primary-800 dark:text-white inline"
                />
            </NavLi>
            <Dropdown class="w-44 z-20">
                <DropdownItem href="/">Profile</DropdownItem>
                <DropdownItem href="/">Login/Register</DropdownItem>
                <DropdownItem href="/">Account Balance Checker</DropdownItem>
                <DropdownItem href="/">Dex Tracker</DropdownItem>
                <DropdownItem href="/">Node Tracker</DropdownItem>
                <DropdownItem href="/">Label Cloud</DropdownItem>
            </Dropdown>
            
        </NavUl>
    </Navbar> -->
    
    
    
    <div class="w-full sticky inset-0 z-[100] flex justify-center bg-[#181818b9] ">
        <nav class=" w-2/3 flex justify-between relative  z-[100] items-center  text-white p-5 " style="font-family: 'Montserrat', sans-serif;">
            <div class="flex space-x-10 w-fit ">
                <a href="/" class="w-fit">
                    <img src="../src/images/ratio2.png" alt="" class="w-1/3">
                </a>
    
    
                <!-- <div class=" w-full flex pr-5">
                    <div class="relative flex items-center">
                        <input type="text" class="h-8 rounded-lg w-56 border-b border-stone-500 outline-none bg-transparent text-white text-xs ">
                        <button class="absolute top-0 right-0 mt-1 mr-1">
                          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5 text-stone-500">
                            <path stroke-linecap="round" stroke-linejoin="round" d="m21 21-5.197-5.197m0 0A7.5 7.5 0 1 0 5.196 5.196a7.5 7.5 0 0 0 10.607 10.607Z" />
                          </svg>
                        </button>
                      </div>
                      
                </div> -->
    
    
            </div>

        
        
        
        
            <!-- svelte-ignore missing-declaration -->
            <ul class="text-white flex items-center space-x-10" style="font-family: 'Montserrat', sans-serif;">
                <li>
                    <h1 class="text-white text-xs ">Home</h1>
    
    
    
                </li>
    
                <!-- svelte-ignore a11y-click-events-have-key-events -->
                <!-- svelte-ignore a11y-no-noninteractive-element-interactions -->
                <li  class="cursor-pointer " on:click={FinanceDrop}>
                    <div class=" flex items-center hover:text-yellow-300 ">
                        <h1 class="text-white text-xs hover:text-yellow-300 hover:font-semibold transition-all">Finance</h1>
                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-4 h-4">
                            <path stroke-linecap="round" stroke-linejoin="round" d="m19.5 8.25-7.5 7.5-7.5-7.5" />
                          </svg>
                          
                    </div>
    
                    {#if dropVisibility}
                    <div class="absolute w-32 flex flex-col pl-2 p-2 rounded-xl shadow-xl space-y-2 mt-4  bg-white text-black  text-xs">
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
                        <div class=" flex items-center hover:text-yellow-300 ">
                        <h1 class="text-white text-xs hover:text-yellow-300 hover:font-semibold transition-all">Tools</h1>
                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-4 h-4">
                            <path stroke-linecap="round" stroke-linejoin="round" d="m19.5 8.25-7.5 7.5-7.5-7.5" />
                          </svg>
                          
                        </div>
    
    
    
                    {#if ToolsVar}
                    <div class="absolute w-32 flex flex-col pl-2 p-2 rounded-xl shadow-xl space-y-2 mt-4  bg-white text-black  text-xs">
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
                    <div class=" flex items-center hover:text-yellow-300 ">
                        <h1 class="text-white text-xs hover:text-yellow-300 hover:font-semibold transition-all">Account</h1>
                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-4 h-4">
                            <path stroke-linecap="round" stroke-linejoin="round" d="m19.5 8.25-7.5 7.5-7.5-7.5" />
                          </svg>
                          
                        </div>
    
    
    
    
    
    
    
    
    
    
    
    
                    {#if AccVar}
                    <!-- svelte-ignore a11y-invalid-attribute -->
                    <div class="absolute w-32 flex flex-col pl-2 p-2 rounded-xl shadow-xl space-y-2 mt-4  bg-white text-black  text-xs">
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
            </ul>
        
        
        </nav>
    
    </div>