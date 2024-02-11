<script>
    import standing from '$lib/images/tanishq-standing.jpg'
    import {onMount} from 'svelte'
    let mobile=false;
    const handleresize=()=>{
        mobile=window.innerWidth<1024;
    }
    onMount(()=>{
        mobile=window.innerWidth<1024;
        window.addEventListener('resize',handleresize)
    });
</script>

<div  id="tanishqdhote" class="w-full  justify-around" style="height:100vh;user-select:none">
    <div class="w-full md:w-4/5 mx-auto flex flex-col md:flex-row md:justify-between pt-20 md:pt-20 px-30" style="height:{mobile?'50vh':'100vh'}">
        
        <div class="w-1/2 flex mx-auto justify-around " ><img src={standing} style="height:{mobile?'50vh':'100vh'};" alt="myself standing"></div>
        <div class="w-{mobile?'4/5 mx-auto':'full'} flex flex-col">
            <p class="text-{mobile?'2xl':'5xl'}" style="font-family:titleFont;align:center"> Hello there👋</p>
            <p class="text-{mobile?'':'xl'}" style="{mobile?'font-size:10px':''};font-family:data;align:center">Myself Tanishq Dhote, I have many interests, I am a meme page admin, a game developer, a web developer, a video game enthusiast and a script writer.</p>
            <p class="text-{mobile?'':'xl'} mt-{mobile?'2':'10'}" style="{mobile?'font-size:10px':''};font-family:data;align:center">I am well versed with Svelte stack, MERN stack, Java(libGDX) for making crossplatform games and Python for automation, datascience and backend. </p>
            
        </div>
    </div>





</div>

<style>

</style>