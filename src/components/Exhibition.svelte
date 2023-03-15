<script>
import { Swiper, SwiperSlide } from 'swiper/svelte';
import { EffectFade,Scrollbar } from 'swiper';
import { Autoplay } from 'swiper/core';
import 'swiper/css/effect-fade';
import 'swiper/css';
import 'swiper/css/scrollbar';
import Saos from 'saos';

const items = [
  {
    title: "sona",
    info: "Autumn 2022 at Kumu Tokyo",
    img: "../image/exhibition_1.jpg"
  },
  {
    title: "CHIQ - Wine × Fragrance",
    info: "Summer 2022 at OFS gallery",
    img: "../image/exhibition_2.jpeg"
  },
  {
    title: "sona",
    info: "Autumn 2022 at Kumu Tokyo",
    img: "../image/exhibition_1.jpg"
  },
  {
    title: "CHIQ - Wine × Fragrance",
    info: "Summer 2022 at OFS gallery",
    img: "../image/exhibition_2.jpeg"
  },
  {
    title: "CHIQ - Wine × Fragrance",
    info: "Summer 2022 at OFS gallery",
    img: "../image/exhibition_2.jpeg"
  },
  {
    title: "sona",
    info: "Autumn 2022 at Kumu Tokyo",
    img: "../image/exhibition_1.jpg"
  },

];


</script>


  <Swiper
      modules={[Scrollbar]}
      speed={1000}
      slidesPerView={"auto"}
      spaceBetween={30}
      scrollbar={{ draggable: true }}
      class="mySwiper wrapper"
  >

  {#each items as item, i}
    <SwiperSlide>
        <div class="swiper-slide">
            <Saos once={true} animation={"zooming 3.0s cubic-bezier(0.2, 0.6, 0.35, 1) both"}>
            <img src={ item.img } alt=""></Saos>
            <div class="info">
              <h3 class="h5" lang="en">{ item.title }</h3>
              <h4 class="h6" lang="en">{ item.info }</h4>
            </div>
        </div>
    </SwiperSlide>

    {/each}


  </Swiper>


<style>

@keyframes -global-zooming {
	0% {transform: scale(1.2);}
  100% {transform: scale(1);}
}
.swiper-slide {
  width: 45vw;
  height: 50vw;
  overflow: hidden;
}
.swiper-slide img {
  width: 45vw;
  height: 50vw;
}
.exhibitions .swiper-slide .info h3 {margin: .5rem 0 .25rem; opacity: .75;}
.exhibitions .swiper-slide .info h4 {opacity: .25;}


@media screen and (min-width: 720px) {
.swiper-slide {
  width: 20vw;
  height: 25vw;
  overflow: hidden;
}
.swiper-slide img {
  width: 20vw;
  height: 25vw;
}
}

</style>