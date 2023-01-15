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
	<title>これまで制作したかほり | atelier sui - 蕊 | 心を澄まして聞くかほり</title>
</svelte:head>

<main class="page">

	<section id="prd">
		
	</section>

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




	
</style>