<script>
import Logo from './Logo.svelte'
</script>

<footer>

</footer>


<style>
    footer {
        width: 100vw;
        padding: 0 5vw 5rem;
        background-color: var(--darkColor);
    }
    footer * {
        color: var(--backgroundColor);
        fill: var(--backgroundColor);
    }
    footer .l-line {
        margin-bottom: 6rem;
        margin-left: -5vw;
    }
    footer .footer-logo {margin-bottom: 5rem;}
    
    ul {margin-bottom: 12rem;}

    footer ul.links li {margin-bottom: .2rem;}
    footer ul.links li:nth-of-type(4) {margin-bottom: 4rem;}
    footer ul.links li.contact {margin-bottom: 2.4rem;}
    footer ul.links li a {font-size: 2.4rem;}
    footer ul.links li.contact a {font-size: 1.8rem;}


    @media screen and (min-width: 720px) {


        footer {
            padding: 0 10vw 5rem;
        }

    }

</style>