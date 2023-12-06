<template>
   <Carousel :breakpoints="breakPrise" :itemsToShow="3" :wrapAround="true" :transition="500">
      <Slide v-for="(item, index) in CarouselSrc" :key="index">
         <div class="carousel__item"><img :src="item.src" :alt="index" />
            <div class="prise">{{ item.prise }} грн</div>
         </div>
      </Slide>

      <template #addons>
         <Navigation />
         <Pagination />
      </template>
   </Carousel>
</template>
<script>
import { defineComponent } from 'vue'

import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel';
import img1 from '@/assets/img/imaga1.png';
import img2 from '@/assets/img/imaga2.png';
import img3 from '@/assets/img/imaga3.png';
import img4 from '@/assets/img/imaga4.png';
import img5 from '@/assets/img/imaga5.png';
import img6 from '@/assets/img/imaga6.png';
import img7 from '@/assets/img/imaga7.png';
import img8 from '@/assets/img/imaga8.png';

export default defineComponent({
   name: 'Autoplay',
   components: {
      Carousel,
      Slide,
      Pagination,
      Navigation,



   },
   data() {
      return {
         CarouselSrc: [{ src: img1, prise: 8300 }, { src: img2, prise: 4100 }, { src: img3, prise: 7550 }, { src: img4, prise: 5700 }, { src: img5, prise: 9900 }, { src: img6, prise: 5200 }, { src: img7, prise: 4500 }, { src: img8, prise: 4000 }],
         breakPrise: {
            0: {
               itemsToShow: 1,
            },
            500: {
               itemsToShow: 2,
            },

            800: {
               itemsToShow: 3,
            },

         },
      };
   },
})
</script>

 
<style scoped>
.prise {
   position: absolute;
   top: 85%;
   left: 85%;
}

.carousel__item {
   position: relative;
   overflow: hidden;
   min-width: 100%;
   max-height: 100%;
}

.carousel__slide {
   background: rgb(255, 255, 255);
   height: 300px;
}

.carousel__viewport {
   perspective: 2000px;
}

.carousel__track {
   transform-style: preserve-3d;
}

.carousel__slide--sliding {
   transition: 0.5s;
}

.carousel__slide {
   opacity: 0.9;
   transform: rotateY(-20deg) scale(0.9);
}

.carousel__slide--active~.carousel__slide {
   transform: rotateY(20deg) scale(0.85);
}

.carousel__slide--prev {
   opacity: 1;
   transform: rotateY(20deg) scale(0.85);
}

.carousel__slide--next {
   opacity: 1;
   transform: rotateY(10deg) scale(0.87);
}

.carousel__slide--active {
   opacity: 1;
   background: linear-gradient(226.12deg, #AAAAAA -1.27%, rgba(255, 255, 255, 0) 137.82%);
   transform: rotateY(0) scale(1.1);
}

@media screen and (max-width: 1220px) {

   .prise {
      position: absolute;
      top: 80%;
      left: 80%;

   }
}

@media screen and (max-width: 900px) {

   .prise {
      position: absolute;
      top: 80%;
      left: 75%;

   }
}
</style>
 