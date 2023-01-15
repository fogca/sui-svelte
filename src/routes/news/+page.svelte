<script>
	//import Saos from "saos";
	//import { Swiper, SwiperSlide } from 'swiper/svelte';
	//import 'swiper/css';
	import Logo from '../../components/Logo@.svelte';
	import Hyphen from '../../components/Hyphen.svelte';
	import Exhibition from '../../components/Exhibition.svelte';
	import Artpiece from '../../components/Artpiece.svelte';
	import Sign from '../../components/Sign.svelte';
	import Saos from 'saos';
	import { onMount } from "svelte";
	import { browser } from "$app/environment";
	import { gsap } from "gsap/dist/gsap";


onMount(() => {

});
</script>

<svelte:head>
	<title>お知らせ | atelier sui - 蕊 | 心を澄まして聞くかほり</title>
</svelte:head>

<main class="page">

	<section id="news">
	  <Saos once={true} animation={"scroll-animation 2.5s cubic-bezier(.6,0,.2,1) both"}>
	  <div class="page-head">
		<div class="h5" lang="en">information</div>
		<h1 class="h2">展示やイベントの<br>お知らせ</h1>
	  </div>
	  </Saos>

	  <Saos once={true} animation={"scroll-animation 2.5s cubic-bezier(.6,0,.2,1) both"}>
	  <div class="wrapper">
		  
	  </div>
	  </Saos>
	</section>

</main>

<style>

.page {
	padding-top: 15rem;
}

@keyframes -global-scroll-animation {
	0% {
		transform: translateY(3px);
		filter: blur(1px);
		opacity: 0;
	}
	100% {
		transform: translateX(0);
		filter: blur(0);
		opacity: 1;
	}
}
@keyframes -global-paragraphy-animation {
	0% {
		transform: translateX(1px);
		filter: blur(5px);
		opacity: 0;
	}
	100% {
		transform: translateX(0);
		filter: blur(0);
		opacity: 1;
	}
}

@keyframes -global-last-animation {
	0% {
		height: 100%;
	}
	100% {
		transform: 100vh;
	}
}



#index-first, #index-second {padding-top: 10rem;}
#index-third {padding-top: 12.5rem;}
#index-fourth {padding-top: 8rem;}

section {position: relative;}

.bg-washi {
	position: fixed;
	width: 100vw;
	height: 100vh;
	/*background-image: url('../image/bg.webp');*/
	background-image: url(/image/bg.webp);
	background-size: cover;
	opacity: .275;
}

#index-top {	
	width: 100vw;
	height: 100vh;
	height: 100svh;
    display: flex;
    align-items: center;
	justify-content: center;
    padding-bottom: 0;
	background-image: url('../image/sui_2023.jpg');
	background-image: url(/image/top.jpg);
	background-size: cover;
}

#index-top .symbol {width: 17.5rem;}

#index-first .wrapper p {margin-top: 1.5rem;}

#index-second .bg {
	width: 100vw;
	margin-top: 4rem;
	margin-left: calc(-1 * var(--padding));
	padding: 12rem 0 11rem;
	padding-left: var(--padding);
	background-image: url('../image/essence.jpg');
	background-image: url(/image/essence.jpg);
	background-size: cover;
}
#index-second .container {margin-bottom: 4.5rem;}
#index-second .container:nth-of-type(3) {margin-bottom: 0;}
#index-second .container h2 {
	font-size: 1.7rem;
	margin-left: -0.5px;
}
#index-second .container h3 {
	opacity: .5;
	margin-top: -.25rem;
	margin-bottom: 1.0rem;
}
#index-second .container p {
	line-height: 2;
	margin-left: -.5px;
	opacity: .9;
}



#index-third .section-head, #index-fourth .section-head {margin-bottom: 1.5rem;}

#index-third .exhibitions {
	width: calc(100vw - var(--padding));
	width: 100%;
	margin-top: 3rem;
}



#index-fourth p {font-size: 1.1rem;}
#index-fourth .exhibitions {
	margin-top: 3rem;
	width: 100vw;
    margin-left: calc(-1 * var(--padding));
}



#index-fifth {margin: 10rem 0 0;}
#index-fifth .logo {width: 16.5rem;margin: 4rem 0;}
#index-fifth .paragraph p {
	line-height: 2.8;
	margin-bottom: 1.6rem;
}
#index-fifth .sign {margin-top: 5rem;}


#index-sixth {
	width: 100vw;
	margin-top: 15rem;
	padding: 10rem var(--padding) 5rem;
	background-image: url('../image/sui_2023.jpg');
	background-image: url(/image/kv.webp);
	background-size: cover;
}
#index-sixth h2 {
	font-size: 1.15rem;
	margin-top: 6rem;}
#index-sixth .mail {margin: 4rem 0 10rem;}
#index-sixth .mail a {border-bottom: solid 0.5px var(--backgroundColor);}
#index-sixth .links ul li {margin-bottom: 1rem;}





 
  
  
  






#index-sixth img {
    width: calc(100% + 6.5vw);
    aspect-ratio: 2/1;
}


	
</style>