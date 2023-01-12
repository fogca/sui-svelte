<svelte:window on:scroll={scrollToWorks} />
<script>
    import { slide } from 'svelte/transition';
    import Saos from "saos";
    import Logo from './Logo.svelte';
    import LogoA from './Logo@.svelte';
    import { browser } from '$app/environment';

    let clicked = false;
	let isExpanded = false
	function clickHandler() {
		isExpanded = !isExpanded  
    }

    function scrollToWorks() {
        if (browser) {
            let header = document.getElementsByTagName('header');
            let currentY = window.pageYOffset;
            let winHeight = window.innerHeight;
            //let set_position = 0;
            window.addEventListener("scroll", () => {
                if ( currentY < winHeight * .5 ) {/* 50vh以下 */
                    header[0].classList.add('top');
                } else if ( currentY > winHeight * .5 && currentY < winHeight * 1.5 ) {/* 50vh以上 && 150vh以下*/
                    header[0].classList.add('show');
                    header[0].classList.remove('top');
                } else if (currentY > winHeight * 1.5 ) {/* 150vh以上 */
                    header[0].classList.remove('show');
                };

                if (currentY < document.documentElement.scrollTop) {
                    header[0].classList.add('down');
                    header[0].classList.remove('up');
                } else {
                    header[0].classList.add('up');
                    header[0].classList.remove('down');
                }
                //set_position = document.documentElement.scrollTop;
                
            });
        }
        
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
    opacity: 0;
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
    transition: .5s ease;
}
header.show {opacity: 1;}

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
