<script>
	//import Saos from "saos";
	//import { Swiper, SwiperSlide } from 'swiper/svelte';
	//import 'swiper/css';
	import Logo from '../../components/Logo@.svelte';
	import TextLogo from '../../components/TextLogo.svelte';
	import Hyphen from '../../components/Hyphen.svelte';
	import Exhibition from '../../components/Exhibition.svelte';
	import Artpiece from '../../components/Artpiece.svelte';
	import Sign from '../../components/Sign.svelte';
	import Saos from 'saos';
	import { onMount } from "svelte";
	import { browser } from "$app/environment";
	import { gsap } from "gsap/dist/gsap";




onMount(() => {
	let pt = document.getElementById('pt');
  	if (browser) {
    	pt.style.visibility = "visible";
  	}
});


</script>

<svelte:head>
	<title>かほりのプロジェクト | atelier sui - 蕊 | 心を澄まして聞くかほり</title>
</svelte:head>


<a href="/" class="logo" data-sveltekit-reload><TextLogo /></a>

<main class="page">
	<div class="bg-washi"></div>
	<section id="pt">
		
		<div class="wrapper">
			<h1 class="h4">かほりのプロジェクト</h1>
			<p>蒸留家・調香師として参画した<br>プロジェクトになります。</p>
		</div>
	</section>

	<section id="pi">
	  <div class="wrapper">

		  <div class="container">
			<div class="image"><img src="../image/projects_senn.jpeg" alt=""></div>
			<h2 class="h2" lang="en">senn - skin care brand</h2>
			<h3 class="h7">スキンケアプロダクト、インセンスの香り</h3>
			<p>本文はデザインや全体のボリューム感を確認するためのダミーテキストです。校正が終了した際は、文章をこちらから置き換えてください。また本文章の文字量が足りない場合は適宜適切な分量をコピーアンドペーストし、ご活用ください。</p>
			<a href="https://shop.sen-n.com/" class="h6" style="text-decoration: underline;">公式サイト</a>
		  </div>

		  <div class="container">
			<img src="../image/projects_senn.jpeg" alt="">
			<h2 class="h2" lang="en">senn - skin care brand</h2>
			<h3 class="h7">スキンケアプロダクト、インセンスの香り</h3>
			<p>本文はデザインや全体のボリューム感を確認するためのダミーテキストです。校正が終了した際は、文章をこちらから置き換えてください。</p>
			<a href="https://sen-n.com/" class="h6" style="text-decoration: underline;">公式サイト</a>
		  </div>

		  <div class="container">
			<img src="../image/projects_senn.jpeg" alt="">
			<h2 class="h2" lang="en">senn - skin care brand</h2>
			<h3 class="h7">スキンケアプロダクト、インセンスの香り</h3>
			<p>本文はデザインや全体のボリューム感を確認するためのダミーテキストです。校正が終了した際は、文章をこちらから置き換えてください。</p>
			<a href="https://sen-n.com/" class="h6" style="text-decoration: underline;">公式サイト</a>
		  </div>
		  
	  </div>
	</section>

</main>

<style>

.bg-washi {opacity: .15;}
.page {padding-bottom: 4rem;}

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

.logo {
	width: 10rem;
	position: absolute;
	top: 4rem;
	left: var(--padding);
}


#pt {
	padding-top: 12.5rem;
	padding-bottom: 5rem;
}

#pt .wrapper p {
    margin-top: 0.5rem;
	font-size: 1.3rem;
    line-height: 2.3;
}

#pi {position: relative;}

#pi .wrapper .container img {width: 100%;}
#pi .wrapper .container:nth-of-type(1) .image {
	width: calc(100vw - var(--padding) + 1px);
	height: calc(100vw - var(--padding));
	
	height: calc(100vh - 125px - 55px - (16px * 2.1) - (13px*2.3*2));
	height: calc(100dvh - (125px + 55px + (16px * 2.1) + (13px*2.3*2)));
	
	margin-bottom: 3rem;
	margin-left: -1px;
	overflow: hidden;
}
#pi .wrapper .container:nth-of-type(1) .image img {
	object-position: 25%;
	width: 100%;
	height: 100%;
	transition: 1s ease-in-out;
}

#pi .wrapper .container {margin-bottom: 8rem;}
#pi .wrapper .container a {
	font-feature-settings: normal;
	letter-spacing: .3em;
}
#pi .wrapper .container h2 {
	margin: 1.5rem 0 .5rem;
	margin-left: -.9px;
}
#pi .wrapper .container h3 {letter-spacing: .3em;}
#pi .wrapper .container p {
	width: 97.5%;
	font-size: 1.25rem;
	opacity: 1;
	margin: 2rem 0 3.5rem;
}



	
</style>