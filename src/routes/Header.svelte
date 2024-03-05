<script>
import dropdownIcon from '$lib/images/drop-down.png'
import {onMount} from 'svelte'
    let mobile=false;
	let dropdownActive=false;
	const handleDropdown=()=>{
		dropdownActive=!dropdownActive
	}
    const handleresize=()=>{
        mobile=window.innerWidth<1024;
    }
    onMount(()=>{
        mobile=window.innerWidth<1024;
        window.addEventListener('resize',handleresize)
    });
</script>
	

<div class="fixed bg-black w-full flex flex-row justify-between md:justify-around px-5 md:px-20 bg-opacity-{mobile?'100':'50'} transition-all ease duration-300 backdrop-blur-sm hover:bg-black" style="height:4rem;z-index:9999;user-select:none;">
	{#if !mobile}
	<a class="text-white text-xl my-auto cursor-pointer" href="#linkedin"><div class="h-full p-4 transition-all ease duration-300 hover:bg-blue-700 rounded" style="font-family:headerFont;">Linked In</div></a>
	<a class="text-white text-xl my-auto cursor-pointer" href="#github"><div class="h-full p-4 transition-all ease duration-300 hover:bg-pink-600 rounded" style="font-family:headerFont">Github</div></a>
	<a class="text-white text-xl my-auto cursor-pointer" href="#youtube"><div class="h-full p-4 transition-all ease duration-300 hover:bg-red-600 rounded" style="font-family:headerFont">Youtube</div></a>
	<a class="text-white text-2xl my-auto cursor-pointer" href="#tanishqdhote"><div class="rounded h-full transition-all ease duration-300 p-4 hover:bg-white hover:text-black" style="font-family:headerFont">Tanishq Dhote </div></a>	
	<a class="text-white text-xl my-auto cursor-pointer" href="#instagram"><div id="instaIcon" class="rounded transition-all ease duration-300 h-full p-4" style="font-family:headerFont">Instagram</div></a>
	<a class="text-white text-xl my-auto cursor-pointer" href="#itchio"><div class="h-full p-4 transition-all ease duration-300 hover:bg-red-500 rounded" style="font-family:headerFont">Itch.io</div></a>
	<a class="text-white text-xl my-auto cursor-pointer" href="#discord"><div class="h-full p-4 transition-all ease duration-300 hover:bg-indigo-600 rounded" style="font-family:headerFont">Discord</div></a>	
	{:else}
	
	<a class="text-white text-2xl my-auto cursor-pointer" href="#tanishqdhote"><div class="rounded transition-all ease duration-300  hover:bg-white hover:text-black" style="font-family:headerFont">Tanishq Dhote </div></a>	
	<button on:click={handleDropdown}><img src={dropdownIcon} style="width:2rem;transform:scale({dropdownActive?'-1':'1'})" alt="dropdown"></button>	

	{#if dropdownActive}
	<div class="w-auto absolute flex flex-col bg-black" style="top:3.5rem;right:0">
			<a class="text-white text-xl my-auto cursor-pointer" href="#linkedin"><div class="h-full p-4 transition-all ease duration-300 hover:bg-blue-700 rounded" style="font-family:headerFont;">Linked In</div></a>
			<a class="text-white text-xl my-auto cursor-pointer" href="#github"><div class="h-full p-4 transition-all ease duration-300 hover:bg-pink-600 rounded" style="font-family:headerFont">Github</div></a>
			<a class="text-white text-xl my-auto cursor-pointer" href="#youtube"><div class="h-full p-4 transition-all ease duration-300 hover:bg-red-600 rounded" style="font-family:headerFont">Youtube</div></a>
			<a class="text-white text-xl my-auto cursor-pointer" href="#instagram"><div id="instaIcon" class="rounded transition-all ease duration-300 h-full p-4" style="font-family:headerFont">Instagram</div></a>
			<a class="text-white text-xl my-auto cursor-pointer" href="#itchio"><div class="h-full p-4 transition-all ease duration-300 hover:bg-red-500 rounded" style="font-family:headerFont">Itch.io</div></a>
			<a class="text-white text-xl my-auto cursor-pointer" href="#discord"><div class="h-full p-4 transition-all ease duration-300 hover:bg-indigo-600 rounded" style="font-family:headerFont">Discord</div></a>	
	</div>
	{/if}	
	{/if}

</div>

<style>
	@font-face {
    font-family: 'headerFont';
    src: url('$lib/fonts/font-.ttf');
  }

  #instaIcon:hover{
	
	background: linear-gradient(45deg, #feda75,#fa7e1e, #d62976,#962fbf,#4f5bd5);
  }

</style>



