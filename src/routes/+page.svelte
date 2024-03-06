<script lang="ts">
	import pageIcon from '$lib/images/tanishq.png'
	import Page1 from './Page1.svelte';
	import Page2 from './Page2.svelte';
	import Page3 from './Page3.svelte';
	import Page4 from './Page4.svelte';
	import Page5 from './Page5.svelte';
	import Page6 from './Page6.svelte';
	import Page7 from './Page7.svelte';
	
</script>

<svelte:head>
	<title>Tanishq Dhote</title>
	<link rel="icon" href={pageIcon} />
	<meta name="description" content="Tanishq Dhote's portfolio website" />
</svelte:head>
	<body class="w-full h-full">
		<Page1/>
		<Page2/>
		<Page3/>
		<Page4/>
		<Page5/>
		<Page6/>
		<Page7/>
	

	</body>
	
<style>
  @font-face {
    font-family: 'titleFont';
    src: url('$lib/fonts/font-10.ttf');
  }
  @font-face {
    font-family: 'headerFont';
    src: url('$lib/fonts/font-7.ttf');
  }
  @font-face {
    font-family: 'data';
    src: url('$lib/fonts/font-9.ttf');
  }
  @font-face {
    font-family: 'subdata';
    src: url('$lib/fonts/font-8.ttf');
  }
</style>
