<script setup>
import Carusel from './components/Carusel.vue';
import imgSebastian from './assets/img/Sebastian.jpg'
</script>

<template>
   <div class="wrapper">
      <header>
         <div class="text_header">ДИЗАЙНЕРСЬКІ СТІЛЬЦІ</div>
      </header>
      <div class="box_carusel">
         <Carusel />
      </div>
   </div>
   <div class="box_text">
      <div class="box_box_text">
         <img class="backdrop-img" :src="imgSebastian" alt="">
         <div class="text">Дизайнерські стільці - це те, чим я завжди хотів займатися у своєму<br>
            житті.<br>
            Я відмінно їх виготовляю та готовий виконати будь-яке ваше побажання<br>
            або виберіть<br>
            із тих,що представлені на моєму сайті. Гарантую швидке та якісне<br>
            виконання. Ви залишитесь задоволені. Дякую за ваш наступний дзвінок! </div>
         <div class="contact">
            <div class="contact_text">Контакти
            </div>
            <div class="num_el">
               <div class="num">+380 97 8037 598</div>
               <div class="el">ivansaparenko4@gmail.com</div>
            </div>
            <div class="atres">вулиця Нестерова, 5, Харків, Харківська область, 61032</div>
         </div>
      </div>
   </div>
</template>

<style scoped>
header {
   width: 100%;
   height: 56px;
   background: #D9D9D9;
   display: flex;
   justify-content: center;
}


.box_carusel {
   background: #D9D9D9;
   margin-top: 30px;
   padding-top: 20px;

}

.text_header {
   margin: auto;
   font-family: url("./assets/IstokWeb-Bold.ttf") format("ttf");
   font-style: normal;
   font-weight: 700;
   font-size: 32px;
   line-height: 46px;
   color: #000000;
}

.wrapper {
   flex: 1;
}

.box_text {
   width: 100vw;
   margin-top: 15px;
   display: flex;
   justify-content: center;
}

.box_box_text {
   position: relative;
   padding-bottom: 50px;
   width: 90%;
   background: #3a3a3a;
   display: flex;
   align-items: center;
   flex-direction: column;
}

.backdrop-img {
   opacity: 0.3;
   position: absolute;
   top: 0;
   left: 0;
   width: 100%;
   min-height: 100%;
}

.text {
   padding: 20px 30px;
   font-family: url("./assets/IstokWeb-Bold.ttf") format("ttf");

   z-index: 10;
   font-family: 'Istok Web';
   font-style: normal;
   font-weight: 400;
   font-size: 32px;
   line-height: 42px;
   text-align: center;

   color: #FFFFFF;


}


.contact {
   font-family: url("./assets/IstokWeb-Bold.ttf") format("ttf");

   z-index: 10;
   display: flex;
   flex-direction: column;
   align-items: center;
   width: 80%;
   gap: 10px;
   color: #ffffff;
   font-size: 24px;
}

.num_el {
   display: flex;
   justify-content: space-between;
   width: 70%;
}

.contact_text {
   font-size: 40px;
   margin: 45px 0;
}

.atres {
   margin-top: 30px;
}

@media screen and (max-width: 900px) {
   .text_header {

      font-size: 25px;

   }

   .text {

      font-size: 25px;

   }

   .contact_text {
      font-size: 30px;
      margin: 25px 0;
   }

   .contact {


      font-size: 18px;
   }

   .num_el {
      display: flex;
      flex-direction: column;
      width: 70%;
   }
}
</style>
