<script>
  import { onMount } from "svelte";
  import Footer from "./footer.svelte";

  import Services from "./services.svelte";
  import Transaction from "./transaction.svelte";
  import NavBar from "../LandingPage/navBar.svelte";
  import Mainbody from "../LandingPage/mainbody.svelte";
  import NewBody from "./newBody.svelte";

  let dropDownOn = false;

  function toggleoptionButton() {
    dropDownOn = !dropDownOn;
    console.log("dropDownOn:", dropDownOn);
  }

  let text =
    "Securing Your Finances, <br> Unleashing Decentralized <br>Possibilities";
  let displayedText = "";

  onMount(() => {
    let index = 0;

    const intervalId = setInterval(() => {
      displayedText = text.substring(0, index + 1);
      index++;

      if (index === text.length) {
        clearInterval(intervalId);
      }
    }, 100);
  });
</script>

<svelte:head>
  <title>DigiPay</title>
  <meta name="description" content="Svelte demo app" />
</svelte:head>

<main class="">
  <NavBar />
  <!-- <Mainbody /> -->
  <NewBody />
  <Footer />
</main>

<!-- 
<section class="" style="background-image: url('../src/images/BGDES.png');  background-size: cover; background-repeat: no-repeat;
background-position: center center;"> -->

<!-- <div class="flex items-center justify-center mt-10 ">


		<div class="flex flex-col items-start ">
			<h1 class="text-5xl font-semibold    mt-8" style="font-family: 'Cormorant Garamond', serif;">
			{@html  displayedText}
			</h1>
	
	
			
			<h5 class="text-sm font-thinflex items-center justify-center  mt-2" style="font-family: 'Montserrat', sans-serif;">
				Web 3.0 Begins
			</h5>
			<button type="button" class="mt-5 text-white w-1/2 justify-center bg-[#FF9119] hover:bg-[#FF9119]/80 focus:ring-4 focus:outline-none focus:ring-[#FF9119]/50 font-medium rounded-lg text-sm px-5 py-2.5 text-center inline-flex items-center dark:hover:bg-[#FF9119]/80 dark:focus:ring-[#FF9119]/40 me-2 mb-2">
				<svg class="w-4 h-4 me-2 -ms-1" aria-hidden="true" focusable="false" data-prefix="fab" data-icon="bitcoin" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><path fill="currentColor" d="M504 256c0 136.1-111 248-248 248S8 392.1 8 256 119 8 256 8s248 111 248 248zm-141.7-35.33c4.937-32.1-20.19-50.74-54.55-62.57l11.15-44.7-27.21-6.781-10.85 43.52c-7.154-1.783-14.5-3.464-21.8-5.13l10.93-43.81-27.2-6.781-11.15 44.69c-5.922-1.349-11.73-2.682-17.38-4.084l.031-.14-37.53-9.37-7.239 29.06s20.19 4.627 19.76 4.913c11.02 2.751 13.01 10.04 12.68 15.82l-12.7 50.92c.76 .194 1.744 .473 2.829 .907-.907-.225-1.876-.473-2.876-.713l-17.8 71.34c-1.349 3.348-4.767 8.37-12.47 6.464 .271 .395-19.78-4.937-19.78-4.937l-13.51 31.15 35.41 8.827c6.588 1.651 13.05 3.379 19.4 5.006l-11.26 45.21 27.18 6.781 11.15-44.73a1038 1038 0 0 0 21.69 5.627l-11.11 44.52 27.21 6.781 11.26-45.13c46.4 8.781 81.3 5.239 95.99-36.73 11.84-33.79-.589-53.28-25-65.99 17.78-4.098 31.17-15.79 34.75-39.95zm-62.18 87.18c-8.41 33.79-65.31 15.52-83.75 10.94l14.94-59.9c18.45 4.603 77.6 13.72 68.81 48.96zm8.417-87.67c-7.673 30.74-55.03 15.12-70.39 11.29l13.55-54.33c15.36 3.828 64.84 10.97 56.85 43.03z"></path></svg>
				Connect Wallet
				</button>
		</div>






	</div>










	
	<div class="flex align-middle justify-center mt-40 ">
		<div class="container flex h-fit p-10">


			<div class="grid">
				<div class="flex">
					<div class="card  space-y-5 flex flex-col align-middle mr-10" style="font-family: 'Montserrat', sans-serif;
				">
					<h1 class="text-white text-2xl font-semibold uppercase" style="font-family: 'Montserrat', sans-serif;
					">Etherium</h1>
					<h1 class="text-sm" style="font-family: 'Montserrat', sans-serif;
					">The live Ethereum price today is $2548.56 USD with a 24-hour trading volume of $24746188474.31 USD.</h1>
	
	
	
	
					<div class=" relative inline-flex">
						<button
			
							type="button" on:click={toggleoptionButton}
							class=" py-3 px-4 inline-flex items-center gap-x-2 text-sm font-medium rounded-lg  text-white bg-[#FF9119]
							  disabled:opacity-50 disabled:pointer-events-none dark:border-gray-700   dark:focus:ring-1 "
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
							class="absolute z-50 shadow-xl transition-[opacity,margin] duration hs-dropdown-open:opacity-100 min-w-[15rem] bg-white  rounded-lg p-2 mt-16 divide-y divide-gray-200 dark:bg-gray-800 dark:border dark:border-gray-700 dark:divide-gray-700"
							aria-labelledby="hs-dropdown-with-icons">
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
										/><path
											d="M10.3 21a1.94 1.94 0 0 0 3.4 0"
										/></svg
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
										/><path d="M12 12v9" /><path
											d="m8 17 4 4 4-4"
										/></svg
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
	 
				<div class="card space-y-11">
					<h1 class="text-white text-xl font-semibold uppercase" style="font-family: 'Montserrat', sans-serif;
					">Converter</h1>
					<h1 class="text-sm" style="font-family: 'Montserrat', sans-serif;
					">Enter the Amount and set the Unit to Convert</h1>
					
	
					<div class="mt-20 flex">
						<input type="text" class="bg-transparent outline-none text-white h-10 rounded-xl ">
						<button type="button" class="ml-2 text-white w-1/2 justify-center bg-[#FF9119] hover:bg-[#FF9119]/80 focus:ring-4 focus:outline-none focus:ring-[#FF9119]/50 font-medium rounded-lg text-sm px-5 py-2.5 text-center inline-flex items-center dark:hover:bg-[#FF9119]/80 dark:focus:ring-[#FF9119]/40 me-2 mb-2">
							<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
								<path stroke-linecap="round" stroke-linejoin="round" d="M19.5 12c0-1.232-.046-2.453-.138-3.662a4.006 4.006 0 0 0-3.7-3.7 48.678 48.678 0 0 0-7.324 0 4.006 4.006 0 0 0-3.7 3.7c-.017.22-.032.441-.046.662M19.5 12l3-3m-3 3-3-3m-12 3c0 1.232.046 2.453.138 3.662a4.006 4.006 0 0 0 3.7 3.7 48.656 48.656 0 0 0 7.324 0 4.006 4.006 0 0 0 3.7-3.7c.017-.22.032-.441.046-.662M4.5 12l3 3m-3-3-3 3" />
							  </svg>
							  
							convert
							</button>
					</div>
				</div>
				</div>






				<form class="w-full mt-20 card1" autocomplete="off" style="font-family: 'Montserrat', sans-serif;" >
					<div class="relative z-0 w-full mb-5 group">
						<input type="email" name="floating_email" id="floating_email" class="block select-none py-2.5 px-0 w-full text-sm text-gray-900 bg-transparent border-0 border-b-2 border-gray-300 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-[#FF9119] peer" placeholder=" " required />
						<label for="floating_email" class="peer-focus:font-medium absolute text-sm text-stone-400 focus:text-[#FF9119] dark:text-gray-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 rtl:peer-focus:left-auto peer-focus:border-[#FF9119]  peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">Address To</label>
					</div>
					<div class="relative z-0 w-full mb-5 group">
						<input type="password" name="floating_password" id="floating_password" class="block py-2.5 px-0 w-full text-sm text-gray-900 bg-transparent border-0 border-b-2 border-gray-300 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-[#FF9119] peer" placeholder=" " required />
						<label for="floating_password" class="peer-focus:font-medium absolute text-sm text-stone-400 focus:text-[#FF9119] dark:text-gray-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 peer-focus:border-[#FF9119] peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">Amount(ETH)</label>
					</div>
					<div class="relative z-0 w-full mb-5 group">
						<input type="password" name="repeat_password" id="floating_repeat_password" class="block py-2.5 px-0 w-full text-sm text-gray-900 bg-transparent border-0 border-b-2 border-gray-300 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-[#FF9119] peer" placeholder=" " required />
						<label for="floating_repeat_password" class="peer-focus:font-medium absolute text-sm text-stone-400 focus:text-[#FF9119] dark:text-gray-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 peer-focus:border-[#FF9119]  peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">Keyword</label>
					</div>

						<div class="relative z-0 w-full mb-5 group">
							<input type="password" name="repeat_password" id="floating_repeat_password" class="block py-2.5 px-0 w-full text-sm text-gray-900 bg-transparent border-0 border-b-2 border-gray-300 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-[#FF9119] peer" placeholder=" " required />
							<label for="floating_repeat_password" class="peer-focus:font-medium absolute text-sm text-[#FF9119] dark:text-gray-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 peer-focus:border-[#FF9119]  peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">Enter Message</label>
						</div>
					
					 
			<button type="button" class="mt-5 text-white w-1/2 justify-center bg-[#FF9119] hover:bg-[#FF9119]/80 focus:ring-4 focus:outline-none focus:ring-[#FF9119]/50 font-medium rounded-lg text-sm px-5 py-2.5 text-center inline-flex items-center dark:hover:bg-[#FF9119]/80 dark:focus:ring-[#FF9119]/40 me-2 mb-2">
				<svg class="w-4 h-4 me-2 -ms-1" aria-hidden="true" focusable="false" data-prefix="fab" data-icon="bitcoin" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><path fill="currentColor" d="M504 256c0 136.1-111 248-248 248S8 392.1 8 256 119 8 256 8s248 111 248 248zm-141.7-35.33c4.937-32.1-20.19-50.74-54.55-62.57l11.15-44.7-27.21-6.781-10.85 43.52c-7.154-1.783-14.5-3.464-21.8-5.13l10.93-43.81-27.2-6.781-11.15 44.69c-5.922-1.349-11.73-2.682-17.38-4.084l.031-.14-37.53-9.37-7.239 29.06s20.19 4.627 19.76 4.913c11.02 2.751 13.01 10.04 12.68 15.82l-12.7 50.92c.76 .194 1.744 .473 2.829 .907-.907-.225-1.876-.473-2.876-.713l-17.8 71.34c-1.349 3.348-4.767 8.37-12.47 6.464 .271 .395-19.78-4.937-19.78-4.937l-13.51 31.15 35.41 8.827c6.588 1.651 13.05 3.379 19.4 5.006l-11.26 45.21 27.18 6.781 11.15-44.73a1038 1038 0 0 0 21.69 5.627l-11.11 44.52 27.21 6.781 11.26-45.13c46.4 8.781 81.3 5.239 95.99-36.73 11.84-33.79-.589-53.28-25-65.99 17.78-4.098 31.17-15.79 34.75-39.95zm-62.18 87.18c-8.41 33.79-65.31 15.52-83.75 10.94l14.94-59.9c18.45 4.603 77.6 13.72 68.81 48.96zm8.417-87.67c-7.673 30.74-55.03 15.12-70.39 11.29l13.55-54.33c15.36 3.828 64.84 10.97 56.85 43.03z"></path></svg>
				Send Money
				</button>
				  </form>
			</div>








			


	
			
		</div>
	
	</div>











	


	 -->

<!-- </section> -->

<!-- <style>

.container {
            max-width: 100%;
            display: flex;
            justify-content: center;
            align-items: center;
            background: #0c0c0c;
            overflow: hidden;
            position: relative;
        }

.card {
  width: 400px;
	min-height: 200px;
  background: rgba( 255, 255, 255, 0.15 );
  box-shadow: 0 8px 32px 0 rgba(255, 115, 0, 0.568);
  backdrop-filter: blur( 18px );
  -webkit-backdrop-filter: blur( 18px );
  border: 1px solid rgba( 255, 255, 255, 0.18 );
  border-radius: 1rem;
  padding: 1.5rem;
  z-index: 10;
  color: whitesmoke;
  
}
.card1{
	background: rgba( 255, 255, 255, 0.15 );
  box-shadow: 0 8px 32px 0 rgba(255, 115, 0, 0.568);
  backdrop-filter: blur( 18px );
  -webkit-backdrop-filter: blur( 18px );
  border: 1px solid rgba( 255, 255, 255, 0.18 );
  border-radius: 1rem;
  padding: 1.5rem;
  z-index: 10;
  color: whitesmoke;
}



</style> -->
