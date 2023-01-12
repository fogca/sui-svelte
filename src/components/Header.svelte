<script>
    import { slide } from 'svelte/transition';
    import Saos from "saos";
    import Logo from './Logo.svelte';
    import LogoA from './Logo@.svelte';

    let clicked = false;
	let isExpanded = false
	function clickHandler() {
		isExpanded = !isExpanded  
    }
	
</script>

<header>
    <div class="top">
        <LogoA />
        <ul>
            <li><a href="/">プロジェクト</a></li>
            <li><a href="/">展示のお知らせ</a></li>
            <li><a href="/">お問い合わせ</a></li>
        </ul>
    </div>

    <div class="bottom"></div>
</header>

<style>

header {

    opacity: 1;

    width: 5rem;
    height: 100vh;
    position: fixed;
    left: auto;
    right: 0;
    top: 0;
    background-image: url(../image/bg.webp);
    background-color:rgba(255,255,255,0.8);
    background-blend-mode:lighten;
    filter: brightness(.95);
    z-index: 9;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
    padding: 3rem 0 5rem;
}

header .top {width: 72.5%;}
header .top ul {margin-top: 4rem;}
header .top ul li {
    margin-left: -2.5px;
    margin-bottom: 1.5rem;
    text-align: center;
}
header .top ul li a {
    writing-mode: vertical-rl;
    vertical-align: center;
    font-feature-settings: initial;
    font-size: 1.1rem;
}


@keyframes -global-header-logo {
	0% {transform: translateY(-.25rem);opacity: 0;}
	100% {transform: translateX(0);opacity: 1;}
}


</style>
