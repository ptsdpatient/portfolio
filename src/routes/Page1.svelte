<script lang="ts">
    import standing from '$lib/images/tanishq.png'
    import {onMount} from 'svelte'
    import Swiper from 'swiper';

    let swiper;

    import mpIcon from '$lib/project/1.jpg?url'
    import danceIcon from '$lib/project/2.jpg?url'
    import sintIcon from '$lib/project/3.jpg?url'
    import snowIcon from '$lib/project/4.jpg?url'
    import boxIcon from '$lib/project/5.jpg?url'
    import adhyayaIcon from '$lib/project/6.jpg?url'
    import chaiIcon from '$lib/project/7.jpg?url'
    import neoadhIcon from '$lib/project/8.jpg?url'
    import bannerImage from '$lib/images/banner.jpg'

    import manga1 from '$lib/manga/1.jpg'
    import manga2 from '$lib/manga/2.jpg'
    import manga3 from '$lib/manga/3.jpg'
    import manga4 from '$lib/manga/4.jpg'
    import manga5 from '$lib/manga/5.jpg'
    import manga6 from '$lib/manga/6.jpg'
    import manga8 from '$lib/manga/8.jpg'
    let mobile=false;

    let selectedTool = 0;


  
   const tools  = [
      {id:1,icon:'/vscode.png',name:'VS Code',link:'',data:'I have been using vs code from a long time for creating web projects'},
      {id:2,icon:'/as.png',name:'Android Studio',link:'',data:''},
      {id:3,icon:'/blender.png',name:'Blender',link:'',data:''},
      {id:4,icon:'/aseprite.png',name:'Aseprite',link:'',data:''},
      {id:5,icon:'/canva.png',name:'Canva',link:'',data:''},
      {id:6,icon:'/cp.png',name:'Clipchamp',link:'',data:''},
      {id:7,icon:'/gc.png',name:'Google Cloud',link:'',data:''},
    ]

    const projects = [
    { id: 1,icon:{mpIcon}, name: 'Microplast Polytex', description: 'Successfully completing the Microplast Polytex website fueled my passion for creating meaningful digital experiences, reinforcing my commitment to excellence as a web developer and anticipating further growth in my journey.',link:'https://www.microplastwovens.com/' },
    { id: 2,icon:sintIcon, name: 'Sintext', description: "My Software is a lightweight and user-friendly text editor designed with the MERN stack, providing a joyful coding experience that won't slow down your computer, ideal for code interviews and DSA competitions, allowing you to customize it to suit your preferences and style.",link:'https://tanishqdhote.itch.io/sintext' },
    { id: 3,icon:snowIcon, name: 'Snow Brick', description: 'Dive into the festive joy of "Opium Bird Christmas Quest," a pixelated Brick Breaker game designed with love using Aseprite, LibGDX, and Android Studio, offering holiday magic, custom blocks, twinkling lights, and delightful surprises for players of all ages.',link:'https://tanishqdhote.itch.io/brickbreak' },
    { id: 4,icon:boxIcon, name: 'Box and Blades', description: "Embark on a thrilling platformer adventure in Box and Blades, where you, as a nimble cardboard box hero, must skillfully dodge menacing blades, utilizing transformative abilities like gliding and turning into steel to conquer each level.",link:'https://tanishqdhote.itch.io/box-and-blades'},
    { id: 5,icon:danceIcon, name: 'PTSD_DANCE', description: 'An engaging and inventive game, inspired by Dance Dance Revolution, crafted using Python and Pygame to challenge players in strategically pressing keys to the rhythm while promoting awareness of PTSD.', link:'https://tanishqdhote.itch.io/ptsdance-revolution' },
    { id: 6,icon:chaiIcon, name: 'Chai Wala', description: 'Navigate inflation challenges, craft diverse teas, set prices, and build relationships as a stranded time traveler in "Time Tea-traveler," a captivating tea stall simulation game set in Nagpur, India, immersing yourself in the citys cultural tapestry to rewrite your destiny and thrive, available on itch.io.',link:'https://tanishqdhote.itch.io/chaiwala'},
    { id: 7,icon:adhyayaIcon, name: 'Adhyaaya24',description:'My work on my college tech fest website. My senior Devansh Parapalli made it in sveltekit, I simply made a few improvements, glad to work as i got an opportunity to show off my skills and enter into domain of svelte.',link:'https://adh24.vercel.app/'},
    { id: 8,icon:neoadhIcon, name: 'NeoAdhyaaya25',description:'Repository for future adhyaaya members. I worked on svelte from scratch in one day so that we could cope up with the routing problem in the main site',link:'https://neo-adhyaaya24.vercel.app/'}
    ];
    const mangas=[
        { id:1,icon:manga1,name:'' },
        { id:2,icon:manga2, name:'' },
        { id:3,icon:manga3,name:'' },
        { id:4,icon:manga4,name:'' },
        { id:5,icon:manga5,name:'' },
        { id:6,icon:manga6, name:'' },
        { id:8,icon:manga8,name:'' },
    ]

   

    const handleresize=()=>{
        mobile=window.innerWidth<1024;
    }
    
    onMount(()=>{
      mobile=window.innerWidth<1024;
      window.addEventListener('resize',handleresize)      
      swiper = new Swiper('.swiper-container', {
      slidesPerView: 'auto',
      grabCursor: true,  
    });
    });

    
</script>






  <div id="tanishqdhote" class="w-full bg-gray-800 flex flex-col md:pt-0 pt-5">
    <div class="bg-blue-700 static"></div>
    <div class="relative w-full md:w-2/3 mx-auto pt-10 md:pt-20"><img src={bannerImage} class=" absolute" style="z-index:0;" alt=""></div>
    
    <div class="w-5/6 md:w-2/3 flex flex-col md:flex-row mx-auto pt-10 md:pt-20">
       <div class="w-full md:w-1/2" style="z-index:1" > <img src={standing} alt=""></div>
      <div class="w-full md:w-1/2 flex flex-col justify-end md:pt-0 pt-5">
        <p class="text-2xl md:text-4xl text-white md:mx-auto title text-left md:text-right"  style="z-index:2;">Hi There! ✌️<br> Myself Tanishq Dhote</p>
      </div>
    </div>

    <div class="w-5/6 text-left md:w-4/6 md:text-center mx-auto flex flex-col">
      <p class="text-white text-2xl md:text-4xl m-10 mb-0 mx-auto title text-left md:text-center" >I am a full stack Web Developer and crossplatform Game Developer</p>
      <p class="text-white text-2xl md:text-3xl m-10 mx-auto title"> I love programming, developing apps and games, and creating concepts for new gaming experiences.</p>
    </div>

    <div class="w-5/6 mx-auto flex flex-col">
      <p class="text-white text-3xl text-center mb-10 md:text-2xl md:text-4xl m-10 mb-0 mx-auto title text-left" >Explore my favorite tools and skills</p>
     
     
    </div>
    
 
    <div class="w-full mx-auto flex flex-wrap gap-5 justify-around ">
      
      {#each tools as tool (tool.id)}

     
      <div id="toolBoxTarget" class="absolute w-full" style="z-index:999">
        {#if selectedTool==tool.id}
      <div class=" bg-white flex flex-col w-full" style="height:100vh">
        <div id="toolBoxTarget" class="w-full flex flex-row justify-between">
          <div class="w-5/6"><p class="text-6xl text-center">{tool.name}</p></div>
          <div class="w-1/6 flex flex-row justify-end" ><button on:click={()=>{selectedTool=0}} class="mt-5 w-1/3 pr-5">
            <img  src="/close.png" alt="">
          </button>
        </div>
          </div>
      </div>
      {/if}
    </div>
  
    {#if selectedTool==0}
      <a href="#toolBoxTarget" class="tools w-3/5 md:w-1/5  gap-5 rounded-2xl bg-white my-5" style="height:15rem">
        <button class='w-full flex h-full py-10 flex-col justify-between' on:click={()=>{selectedTool=tool.id}} >    
    
        <img class="mx-auto" style="max-width:50%" src={tool.icon} alt="">
        <p class="w-full text-center text-2xl mx-auto">{tool.name}</p>
      </button>
    </a>
    {/if}
      {/each}
    </div>
  </div>



<style>
  .tools{
    transition: all 0.4s;
  }
  .tools:hover{
    transform: scale(1.1);
    transition: all 0.4s;
  }
  #tanishqdhote{     
      background-image: url('/pattern2.png');
      background-repeat: repeat;
  }
  .title{
    font-family:data;
  }
  .swiper-container {
    width: 100%;
  
    overflow: hidden;
  }

  .swiper-wrapper {
    display: flex;

    transition: transform 0.3s ease-in-out;
  }

  .swiper-slide {

    box-sizing: border-box;
  }

  .project-card {
    /* Customize your project card styles */
    padding: 16px;
    border: 1px solid #ddd;
    border-radius: 8px;
    background-color: #fff;
  }
</style>