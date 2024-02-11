<script>
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

    let mobile=false;
    const projects = [
    { id: 1,icon:mpIcon, name: 'Microplast Polytex', description: 'Successfully completing the Microplast Polytex website fueled my passion for creating meaningful digital experiences, reinforcing my commitment to excellence as a web developer and anticipating further growth in my journey.',link:'https://www.microplastwovens.com/' },
    { id: 2,icon:sintIcon, name: 'Sintext', description: "My Software is a lightweight and user-friendly text editor designed with the MERN stack, providing a joyful coding experience that won't slow down your computer, ideal for code interviews and DSA competitions, allowing you to customize it to suit your preferences and style.",link:'https://tanishqdhote.itch.io/sintext' },
    { id: 3,icon:snowIcon, name: 'Snow Brick', description: 'Dive into the festive joy of "Opium Bird Christmas Quest," a pixelated Brick Breaker game designed with love using Aseprite, LibGDX, and Android Studio, offering holiday magic, custom blocks, twinkling lights, and delightful surprises for players of all ages.',link:'https://tanishqdhote.itch.io/brickbreak' },
    { id: 4,icon:boxIcon, name: 'Box and Blades', description: "Embark on a thrilling platformer adventure in Box and Blades, where you, as a nimble cardboard box hero, must skillfully dodge menacing blades, utilizing transformative abilities like gliding and turning into steel to conquer each level.",link:'https://tanishqdhote.itch.io/box-and-blades'},
    { id: 5,icon:danceIcon, name: 'PTSD_DANCE', description: 'An engaging and inventive game, inspired by Dance Dance Revolution, crafted using Python and Pygame to challenge players in strategically pressing keys to the rhythm while promoting awareness of PTSD.', link:'https://tanishqdhote.itch.io/ptsdance-revolution' },
    { id: 6,icon:chaiIcon, name: 'Chai Wala', description: 'Navigate inflation challenges, craft diverse teas, set prices, and build relationships as a stranded time traveler in "Time Tea-traveler," a captivating tea stall simulation game set in Nagpur, India, immersing yourself in the citys cultural tapestry to rewrite your destiny and thrive, available on itch.io.',link:'https://tanishqdhote.itch.io/chaiwala'},
    { id: 7,icon:adhyayaIcon, name: 'Adhyaaya24',description:'My work on my college tech fest website. My senior Devansh Parapalli made it in sveltekit, I simply made a few improvements, glad to work as i got an opportunity to show off my skills and enter into domain of svelte.',link:'https://adh24.vercel.app/'},
    { id: 8,icon:neoadhIcon, name: 'NeoAdhyaaya25',description:'Repository for future adhyaaya members. I worked on svelte from scratch in one day so that we could cope up with the routing problem in the main site',link:'https://neo-adhyaaya24.vercel.app/'}
];


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

<div  id="tanishqdhote" class="w-full  justify-around" style="user-select:none">
    <div class="w-full mx-auto flex flex-col md:flex-row md:justify-between pt-20 md:pt-20">
        
        <div class="w-4/5 md:w-2/5 bg-blue flex mx-auto justify-around " ><img src={standing}  alt="myself standing"></div>
        <div class="w-full md:w-3/5 px-10 mx-auto flex flex-col">
            <p class="text-{mobile?'2xl':'5xl'} mx-auto" style="font-family:titleFont;text:center;align:center"> Hello there👋</p>
            <p class="text-{mobile?'sm':'2xl'}" style="{mobile?'font-size:xl':''};font-family:data;align:center">Myself Tanishq Dhote, I have many interests, I am a meme page admin, a game developer, a web developer, a video game enthusiast and a script writer.</p>
            <p class="text-{mobile?'sm':'2xl'} mt-{mobile?'2':'10'}" style="{mobile?'font-size:xl':''};font-family:data;align:center">I am well versed with Svelte stack, MERN stack, Java(libGDX) for making crossplatform games and Python for automation, datascience and backend. </p>
            
        </div>

    </div>

    <div class="w-full md:w-4/5 mx-auto flex flex-col md:justify-between md:pt-20 px-30 " >
        <p class="text-{mobile?'3xl':'5xl'} mx-auto my-5" style="font-family:titleFont;text:center;align:center"> My projects 💻</p>
       
        <div class="swiper-container">
            <div class="swiper-wrapper">
              {#each projects as project (project.id)}
                <div class="swiper-slide h-full" style="min-width: {mobile?'50vw':'20vw'};">
                  <div class="project-card">
                    <div class="projectCard" style="min-width: {mobile?'50vw':'10vw'};">
                        <button on:click={()=>window.open(project.link)}><img src={project.icon} alt={project.name}></button>
                        <h3 class="text-{mobile?'xl':'2xl'}" style="font-family:headerFont">{project.name}</h3>
                    </div>        
                  </div>
                </div>
              {/each}
            </div>
          </div>
     
        

    </div>





</div>

<style>
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