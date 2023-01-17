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

});
</script>

<svelte:head>
	<title>これまで制作したかほり | atelier sui - 蕊 | 心を澄まして聞くかほり</title>
</svelte:head>

<main class="page">

	<section id="pt">
		<a href="/" class="logo"><TextLogo /></a>
		<div class="wrapper">
			<h1 class="h4">かほりのプロジェクト</h1>
			<p>蒸留家・調香師として参画した<br>プロジェクトになります。</p>
		</div>
	</section>

	<section id="pi">
	  <div class="wrapper">

		  <div class="container">
			<img src="../image/about.jpg" alt="">
			<h2 class="h3" lang="en">senn - skin care brand</h2>
			<p>山の花は、多治見をはじめとする「東濃」で作られるやきものを常設販売する器のセレクショップです。作家モノを中心に、地元メーカーの工業製品やオブジェまで幅広く取り扱い、東濃のやきもののクオリティの高さと多様性を楽しむことができます。</p>
			<a href="https://sen-n.com/" class="h6" style="text-decoration: underline;">公式サイト</a>
		  </div>

		  <div class="container">
			<img src="../image/about.jpg" alt="">
			<h2 class="h3" lang="en">senn - skin care brand</h2>
			<p>山の花は、多治見をはじめとする「東濃」で作られるやきものを常設販売する器のセレクショップです。作家モノを中心に、地元メーカーの工業製品やオブジェまで幅広く取り扱い、東濃のやきもののクオリティの高さと多様性を楽しむことができます。</p>
			<a href="https://sen-n.com/" class="h6" style="text-decoration: underline;">公式サイト</a>
		  </div>

		  <div class="container">
			<img src="../image/about.jpg" alt="">
			<h2 class="h3" lang="en">senn - skin care brand</h2>
			<p>山の花は、多治見をはじめとする「東濃」で作られるやきものを常設販売する器のセレクショップです。作家モノを中心に、地元メーカーの工業製品やオブジェまで幅広く取り扱い、東濃のやきもののクオリティの高さと多様性を楽しむことができます。</p>
			<a href="https://sen-n.com/" class="h6" style="text-decoration: underline;">公式サイト</a>
		  </div>
		  
	  </div>
	</section>

</main>

<style>

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

#pt {
	height: calc(100vh - (100vw - var(--padding) + var(--padding)));
	padding-top: 4rem;
	position: relative;
}
#pt .logo {width: 13rem;}
#pt .wrapper {
	position: absolute;
	top: auto;
	bottom: 6rem;
}
#pt .wrapper p {
	opacity: .75;
    margin-top: 0.5rem;
}

#pi .wrapper .container:nth-of-type(1) img {
	width: calc(100vw - var(--padding));
	height: calc(100vw - var(--padding));
	margin-bottom: 3rem;
}
#pi .wrapper .container:nth-of-type(1) h2 {margin: 0;}

#pi .wrapper .container {margin-bottom: 8rem;}
#pi .wrapper .container a {font-feature-settings: normal;}
#pi .wrapper .container h2 {margin: 2.5rem 0 1rem;}
#pi .wrapper .container p {
	width: 97.5%;
	font-size: 1.15rem;
	opacity: .75;
	margin: .5rem 0 3rem;
}



	
</style>