<script>
import { Swiper, SwiperSlide } from 'swiper/svelte';
import { EffectFade } from 'swiper';
import { Autoplay } from 'swiper/core';
import 'swiper/css/effect-fade';
import 'swiper/css';

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
  }
  ];


</script>



<Swiper
    loop={true}
    autoplay={{
        delay: 5000,
        disableOnInteraction: true
    }}
    speed={5000}
    modules="{[EffectFade, Autoplay]}" effect="fade"
  >
  {#each items as item, i}
    <SwiperSlide>
        <div class="swiper-slide">
            <img src={ item.img } alt="">
            <div class="info">
              <h3 class="h5" lang="en">{ item.title }</h3>
              <h4 class="h6" lang="en">{ item.info }</h4>
            </div>
        </div>
    </SwiperSlide>

    {/each}


  </Swiper>


<style>

.swiper-slide img {
    width: 100vw;
    width: 100%;
    height: 80vw;
}
.exhibitions .swiper-slide .info h3 {margin: .5rem 0 .25rem; opacity: .75;}
.exhibitions .swiper-slide .info h4 {opacity: .25;}
</style>