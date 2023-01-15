<script>
//import { page } from '$app/stores';
//import PageTransition from '../components/PageTransition.svelte';  
import { page } from '$app/stores';
import Header from '../components/Header.svelte';
import Footer from '../components/Footer.svelte';
import LocomotiveScrollProvider from 'svelte-locomotive-scroll';
//import 'locomotive-scroll/src/locomotive-scroll.scss';


/* @type {import('./$types').LayoutData} */
    //export let data;
    //$: currentRoute = $page.url.pathname; 
</script>
  
<svelte:head>
  <link rel="stylesheet" href="../css/base.css">
  <link rel="stylesheet" href="../css/main.css">
  <link rel="stylesheet" href="../css/layout.css">
  <link rel="stylesheet" href="../css/prerendering.css">
  <link rel="stylesheet" href="https://use.typekit.net/alu3vih.css"><!--Adobe Fonts-->
  <script src="https://webfont.fontplus.jp/accessor/script/fontplus.js?kqbwQX--jVA%3D&box=3PQPrveWeX4%3D&aa=1&ab=2"></script>
</svelte:head>
  
<div>
  <LocomotiveScrollProvider
	options={{
		smooth: true,
		smoothMobile: true,
		getDirection: true,
		getSpeed: true,
		inertia: 0.5
	}}
	watch={$page}
	location={$page.url}
	onLocationChange={(scroll) => scroll.scrollTo(0, { duration: 2, disableLerp: false })}
	imageTarget={'.grid-item-media'}
>

    <Header></Header>
      <slot />
    <Footer></Footer>

</LocomotiveScrollProvider>
  
  </div>
  