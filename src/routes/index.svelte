<script>
	import Saos from "saos";
	import { Swiper, SwiperSlide } from 'swiper/svelte';
	import 'swiper/css';
	import Logo from '../components/Logo@.svelte';
	import Exhibition from '../components/Exhibition.svelte';
	import Artpiece from '../components/Artpiece.svelte';
	import Sign from '../components/Sign.svelte';

</script>

<svelte:head>
	<title>蕊 atelier sui | 心を澄まして聞くかほり</title>
</svelte:head>

<main>
	<Logo />
	<div class="bg">
	<section id="index-top">
        <Saos animation={"opening-img 1.5s cubic-bezier(0.3, 0, 0.7, 1) both"} once={true}></Saos>
	</section>

	<section id="index-first">
	  <div class="section-head">
		<span class="h5" lang="en">01.</span>
		<h1 class="h2" lang="en">fragrance</h1>
	  </div>
	  <div class="wrapper">
		<p class="h5">心を澄まして聞くかほり</p>
		<p class="h5">素材との出会いから、抽出、調香まで<br>
		  万物に内在する響きを掬いとり<br>
		  いのちが共鳴するような時間を
		</p>
		<p class="h4" lang="en" style="margin-top: 1.25rem;">is consistent from material search, <br>extraction to distillation.</p>
	  </div>
	</section>

	<section id="index-second" class="white">
	  <div class="section-head">
		<span class="h5" lang="en">02.</span>
		<h1 class="h2" lang="en">essence</h1>
	  </div>
	  <div class="container">
		<h2 class="h4">自然の音色を聞く</h2>
		<h3 class="h4" lang="en">extract</h3>
		<p>植物や素材の記憶に耳を澄まし<br>寄り添いながら香りを抽出</p>
	  </div>
	  <div class="container">
		<h2 class="h4">心の声を聞く</h2>
		<h3 class="h4" lang="en">blend</h3>
		<p>人それぞれの祈りや記憶と<br>響き合う余韻のある調香</p>
	  </div>
	  <div class="container">
		<h2 class="h4">物語を聞く</h2>
		<h3 class="h4" lang="en">ensemble</h3>
		<p>体験や空間が纏う空気を掬い<br>ともに奏でるコラボレーション</p>
	  </div>
	</section>
	</div>

	<section id="index-third" class="js-scroll">
	  <div class="section-head">
		<span class="h5" lang="en">03.</span>
		<h1 class="h2" lang="en">experience</h1>
		<h2 class="h6">各地で行わせていただいた展示や<br>ワークショップの一部をご紹介します。</h2>
	  </div>

	  <div class="swiper exhibitions white">
		<Exhibition />
	  </div>
	</section>

	<section id="index-fourth">
	  <div class="section-head">
		<span class="h5" lang="en">04.</span>
		<h1 class="h2" lang="en">art piece</h1>
		<h2 class="h6">様々なご縁でめぐり合った素材から<br>製作した作品のアーカイブ。<br>
		  一部、販売しているものもございます。</h2>
	  </div>

	  <div class="swiper exhibitions white">
		  <Artpiece />
	  </div>

	</section>

	<section id="index-fifth">
	  <div class="section-head">
		<span class="h5" lang="en">05.</span>
		<h1 class="h2" lang="en">about</h1>
		<h2 class="h4">かほりとともに</h2>
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

.bg {
	width: 100vw;
	min-height: 100vh;
	height: fit-content;
	background-image: url('../image/sui_bg.jpg');
	background-size: cover;
}
.bg * {color: white;}

#index-top {
    min-height: calc(var(--vh, 1vh) * 100);
    display: flex;
    align-items: flex-end;
    padding-bottom: 6.5rem;
  }

  #index-first, #index-third {
    padding-top: 10rem;
    padding-bottom: 12rem;
  }
  #index-first .wrapper p.h5 {margin-top: 1rem;}

  #index-second {
    padding-top: 10rem;
    padding-bottom: 7.5rem;
  }
  #index-second .container {margin-bottom: 5.6rem;}
  #index-second .container h2 {margin-left: -.23rem;}
  #index-second .container p {margin-left: -.05rem;}
  #index-second .container h3 {margin-bottom: 1.2rem;}

  .exhibitions {
	width: 100vw;
    margin-left: calc( var(--padding) * -1 );
  }

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