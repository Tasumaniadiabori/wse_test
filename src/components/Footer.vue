<template lang="pug">
.footer-background
  .footer-container 
    .top
      img(src='Logo.svg')
      .logo-text 
        p.first-part Webcam studio
          span.second-part  expert
      .button
        .one Каталог и сертификация вебкам-студий
      .button
        .two Каталог студий
    .bottom
      .button Индивидуальный подбор студии
      .button Полезные ссылки
      .button Добавить студию
      .button Сертификация
      .button Оставить жалобу
      .button Обратная связь
      .trademark © 2021 webcam-studio.expert
      .button Пользовательское соглашение
      .button Политика конфиденциальности
</template>

<script lang="ts">
import Vue from 'vue'
import Component from 'vue-class-component'

@Component
export default class Footer extends Vue {}
</script>

<style>
@media only screen and (max-width: 1360px) {
  .footer-background {
    width: 1024px;
    max-height: 277px;
  }
  .bottom {
    grid-template-columns: 322px 326px 348px;
  }
}
@media only screen and (min-width: 1360px) {
  .footer-background {
    width: 1360px;
    max-height: 277px;
  }
  .bottom {
    grid-template-columns: 414px 376px 542px;
  }
}
.footer-background {
  display: flex;
  flex: 1;
  background: linear-gradient(180deg, #313136 0%, #674780 100%);
  box-shadow: 0px 0px 30px rgba(91, 91, 131, 0.02);
}
.footer-container {
  max-width: 100%;
  display: flex;
  flex-direction: column;
  justify-items: flex-end;
  padding: 36px 44px 0px 44px;
  border-bottom: 37px solid rgba(0, 0, 0, 0.2);
}
.top {
  max-width: 100%;
  display: flex;
  flex-direction: row;
  padding: 0px 14px 32px 14px;
  align-items: center;
  border-bottom: 1px solid rgba(196, 196, 196, 0.1);
}
.logo-text {
  display: flex;
  flex-direction: row;
  font-family: Hind;
  font-style: normal;
  font-weight: normal;
  font-size: 26px;
  line-height: 42px;
  text-transform: uppercase;
  margin-left: 16px;
  cursor: pointer;
}
.logo-text:hover {
  text-decoration: underline;
  text-decoration-color: #fefeff;
}
.logo-text .first-part {
  color: #ff93cd;
  
}
.logo-text .second-part {
  color: #7bd0ff;
}
.button {
  font-family: Manrope;
  font-style: normal;
  font-weight: normal;
  font-size: 14px;
  line-height: 17px;
  color: #fefeff;
  cursor: pointer;
}
.button:hover {
  text-decoration: underline;
}
.button .one {
  font-size: 16px;
  line-height: 20px;
  color: #aa9ab8;
  margin-left: 78px;
}
.button .two {
  font-size: 16px;
  line-height: 20px;
  margin-left: 72px;
}
.bottom {
  display: grid;
  align-items: center;
  grid-template-rows: 0px 64px 72px 20px;
  padding: 45px 14px 0px 14px;
}
.trademark {
  font-family: Manrope;
  font-style: normal;
  font-weight: normal;
  font-size: 14px;
  line-height: 17px;
  color: #aa9ab8;
}
</style>
