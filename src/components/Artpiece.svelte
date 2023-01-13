<script>
	import { Swiper, SwiperSlide } from 'swiper/svelte';
    import { EffectFade } from 'swiper';
    import { Autoplay } from 'swiper/core';
    
    import 'swiper/css/effect-fade';
	import 'swiper/css';

    const items = [
    {
      title: "香水びん",
      img: "../image/exhibition_1.jpg"
    },
    {
      title: "kousui binn",
      img: "../image/exhibition_2.jpeg"
    },
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
              <h3 class="p" lang="en">{ item.title }</h3>
            </div>
        </div>
    </SwiperSlide>

    {/each}


  </Swiper>


<style>

.swiper-slide img {
    width: 100%;
    height: 100vw;
}

.info {margin-left: var(--padding);}

.swiper-slide h3 {
  font-size: 1.1rem;
  opacity: .5;
}
</style>