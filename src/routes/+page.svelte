<script>
	import Saos from "saos";
	import { Swiper, SwiperSlide } from 'swiper/svelte';
	import 'swiper/css';
	import Logo from '../components/Logo@.svelte';
	import Hyphen from '../components/Hyphen.svelte';
	import Exhibition from '../components/Exhibition.svelte';
	import Artpiece from '../components/Artpiece.svelte';
	import Sign from '../components/Sign.svelte';

</script>

<svelte:head>
	<title>atelier sui - 蕊 | 心を澄まして聞くかほり</title>
</svelte:head>

<main>
	
	<div class="bg-washi"></div>
	<section id="index-top">
		<div class="symbol"><Logo /></div>
	</section>

	<section id="index-first">
	  <div class="section-head">
		<span class="h4" lang="en">01.</span>
		<Hyphen />
		<h1 class="h4" lang="en">fragrance</h1>
	  </div>
	  <div class="wrapper">
		<h2 class="h2">心を澄まして<br>聞くかほり</h2>
		<p class="h5">素材との出会い、抽出、調香まで<br>
			小さないのちに内在する響きから<br>
			季節や風土のめぐりに触れる香りづくり
		</p>
	  </div>
	</section>

	<section id="index-second">
	  <div class="section-head">
		<span class="h4" lang="en">02.</span>
		<Hyphen />
		<h1 class="h4" lang="en">essence</h1>
	  </div>
	  <div class="bg">
	  	<div class="container white">
			<h2 class="h4">自然の音色を聞く</h2>
			<h3 class="h4" lang="en">extract</h3>
			<p>暦や土地によって変化する植物の声に<br>耳を澄ましてその本質を抽出</p>
	  	</div>
	  	<div class="container white">
			<h2 class="h4">心の声を聞く</h2>
			<h3 class="h4" lang="en">blend</h3>
			<p>それぞれの感性をひらき<br>心に響く余韻のある調香</p>
	  	</div>
	  	<div class="container white">
			<h2 class="h4">物語を聞く</h2>
			<h3 class="h4" lang="en">ensemble</h3>
			<p>体験や空間が纏う空気を掬い<br>ともに奏でるコラボレーション</p>
	  	</div>
	  </div>
	</section>
	

	<section id="index-third" class="js-scroll">
	  <div class="section-head">
		<span class="h4" lang="en">03.</span>
		<Hyphen />
		<h1 class="h4" lang="en">experience</h1>
	  </div>
	  <h2 class="p">各地で行わせていただいた展示や<br>ワークショップの一部をご紹介します。</h2>

	  <div class="swiper exhibitions">
		<Exhibition />
	  </div>
	</section>

	<section id="index-fourth">
	  <div class="section-head">
		<span class="h4" lang="en">04.</span>
		<Hyphen />
		<h1 class="h4" lang="en">art piece</h1>
	  </div>
	  <h2 class="p">様々なご縁でめぐり合った素材から<br>製作した作品のアーカイブ。</h2>
	  <p style="opacity: .5;" class="h6">一部、販売しているものもございます。</p>

	  <div class="swiper exhibitions">
		  <Artpiece />
	  </div>

	</section>

	<section id="index-fifth">
	  <div class="section-head">
		<span class="h4" lang="en">05.</span>
		<Hyphen />
		<h1 class="h4" lang="en">about</h1>
	  </div>
	  <p>
	  2012年創立<br>
	  日本発のナチュラルフレグランスブランド。<br><br>

	  幼少期から音楽を続けていた調香師が、<br>
	  植物の香りと出逢い、情景や記憶との<br>結びつきを体感。<br><br>

	  自然に内在する”響き”を奏でるような、<br>
	  抽出、調香の実験をはじめました。<br><br>

	  日本の豊かな素材と香文化、<br>西洋の歴史ある香水文化。<br>
	  それぞれの魅力を織り交ぜた<br>作品を特徴としています。<br><br>

	  風のように偶然性と余白のある、かほり。<br><br>

	  だからこそ生まれる、人々との共鳴を<br>喜びとし、
	  おひとりおひとりに<br>届けられたらと願っています。
	  </p>
	  <Sign />
	  
	</section>


	<section id="index-sixth">
	  <img data-src="assets/image/kv.webp" alt="" class="lazyload">
	  <div class="section-head">
		<span class="h5" lang="en">06.</span>
		<h1 class="h2" lang="en">contact</h1>
		<h2 class="h5">蒸留・調香に関するご相談・ご質問は<br>
		  以下メールアドレスよりお問い合わせください。<br>
		  またオーダー・パーソナルフレグランスも<br>
		  承っておりますので、是非ご相談ください。</h2>
	  </div>
	  <div class="mail">
		<a href="" class="h4" lang="en">info@kahoritotomoni.com</a>
	  </div>
	</section>
	
</main>

<style>

@keyframes -global-scroll-animation {
	0% {transform: translateY(1.5rem);opacity: 0;}
	100% {transform: translateX(0);opacity: 1;}
}
@keyframes -global-opening {
	0% {transform: translateY(.5rem);opacity: 0;filter: blur(10px);}
	100% {transform: translateX(0);opacity: 1;filter: blur(0);}
}
@keyframes -global-opening-img {
	0% {filter: saturate(0);}
	100% {filter: saturate(1);}
}

#index-first, #index-second {padding-top: 10rem;}
#index-third {padding-top: 12.5rem;}
#index-fourth {padding-top: 8rem;}

section {position: relative;}

.bg-washi {
	position: fixed;
	width: 100vw;
	height: 100vh;
	background-image: url('../image/bg.webp');
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
	background-size: cover;
}

#index-first .wrapper p {margin-top: 1.5rem;}

#index-second .bg {
	width: 100vw;
	margin-top: 4rem;
	margin-left: calc(-1 * var(--padding));
	padding: 8rem 0 2.5rem;
	padding-left: var(--padding);
	background-image: url('../image/essence.jpg');
	background-size: cover;
}

#index-second .container h3 {
	opacity: .5;
	margin-top: -.25rem;
}

#index-third .section-head, #index-fourth .section-head {margin-bottom: 1.5rem;}

#index-third .exhibitions {
	width: calc(100vw - var(--padding));
	margin-top: 3rem;
}

#index-fourth p {font-size: 1.1rem;}
#index-fourth .exhibitions {margin-top: 3rem;}









 
  #index-second .container {margin-bottom: 5.6rem;}
  #index-second .container h2 {margin-left: -.23rem;}
  #index-second .container p {margin-left: -.05rem;}
  #index-second .container h3 {margin-bottom: 1.2rem;}



#index-fifth {margin: 10rem 0 10rem;}

#index-fifth svg {margin-top: 4rem;}

#index-sixth img {
    width: calc(100% + 6.5vw);
    aspect-ratio: 2/1;
}
#index-sixth .section-head {margin-top: 5rem;}
#index-sixth .mail {margin-top: 6rem;}
#index-sixth .mail a {border-bottom: solid 0.5px var(--textColor);}

	
</style>