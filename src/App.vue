<template>
  <v-app>
    <router-view />
  </v-app>
</template>
<script>
//import Contenedor from '@/views/content/contenedor/Contenedor.vue';
export default {
  components: {},
  data() {
    return {};
  },
};

</script>

<style>
main {
  padding-top: 0px !important;
}
.v-sheet.theme--light.elevation-7.v-toolbar.v-app-bar.v-app-bar--fixed{
  background-color: #ffc107 !important;
}
.color-drawer.v-navigation-drawer.v-navigation-drawer--fixed.v-navigation-drawer--mini-variant.v-navigation-drawer--open.v-navigation-drawer--open-on-hover.theme--light{
  
}
.text-white.text-bold.banner-text{
color:#585858  !important;
}
.v-icon.notranslate.mdi.mdi-bell.theme--light{
  color:#343a40  !important;
}
.v-icon.notranslate.mdi.mdi-dots-vertical.theme--light{
  color:#343a40  !important;
}
.v-list.scroll.v-sheet.theme--light.v-list--three-line{
background-color:#ffc107;
color:White;
}
.v-list-item__content div{
color:#585858 !important;
}
.v-menu__content.theme--light.v-menu__content--fixed.menuable__content__active > .theme--light.v-list{
  background-color:#ffc107 !important;
}
.v-menu__content.theme--light.v-menu__content--fixed.v-menu-transition-leave-active.v-menu-transition-leave-to{
  background-color:#ffc107 !important;
}
.v-list-item--active.v-list-item.v-list-item--link.theme--light div i{
color:#131b1e !important;
}
.v-list-item--active.v-list-item.v-list-item--link.theme--light > .v-list-item__title{
color:#131b1e !important;
}
*{
  text-decoration: none !important;
}
nav .v-list-item.theme--light > div > div{
  color:white !important;
}
.px-2.v-list-item--active.v-list-item.v-list-item--link.theme--light > .v-list-item.theme--light > div > div{
color:#131b1e !important;
}
.v-main__wrap{
  background-image: url(/img/jovenes11.eddac1d6.webp) !important;
    background-size: cover !important;
    background-position:fixed !important;
    background-repeat: no-repeat !important;
}
.v-application.v-application--is-ltr.theme--light{
  background-image: url(/img/jovenes11.eddac1d6.webp) !important;
    background-size: cover !important;
    background-position:fixed !important;
    background-repeat: no-repeat !important;
}

.no-result.sad-face > span{
color: #ffc107 !important;
}
.no-result::before{
color: #ffc107 !important;
}
.m-0.font-weight-bold{
  color: #ffc107 !important;
}







:root {
  --bg-color: #f8f8f8;
  --color-white: #464040;
  --first-color-gray: #ecf0f3;
  --second-color-gray: #9d9d9d;
  --purple-color: #9fbdf8;
  --first-color-green: #ffc107;
  --second-color-green: #59a350;
  --third-color-green: #448f3c;
  --fourth-color-green: #20421c;
  --fifth-color-green: #324230;
  --sixth-color-green: #343a40;
  --bg-btn: linear-gradient(180deg, #69ea58 -166.98%, #31bd1f 143.4%);
  --seventh-color-green: #1d2528;
  --eighth-color-green: #29343a;
  --bg-btn: linear-gradient(180deg, #1eff00 -166.98%, #54af47 143.4%);
  --bg-content: #f5f3f3;
}

* {
  font-family: "Segoe UI", Helvetica, Arial, sans-serif;
}

#app {
  /* width: 100vw;
  height: 100vh; */
  background-color: var(--bg-content);
  /* overflow: scroll; */
}

.v-application .success--text {
  color: #f8bc02 !important;
  caret-color: #f8bc02 !important;
}

::-webkit-scrollbar-track {
  -webkit-box-shadow: inset 0 0 6px #ffc107;
  box-shadow: inset 0 0 6px #ffc107;
  border-radius: 10px;
  background-color: #f5f5f5;
}

::-webkit-scrollbar {
  width: 12px;
  background-color: #f5f5f5;
}

::-webkit-scrollbar-thumb {
  border-radius: 10px;
  -webkit-box-shadow: inset 0 0 6px #ffc107;
  box-shadow: inset 0 0 6px #ffc107;
  background-color: #ffc107;
}

/* ::-webkit-scrollbar,
.scroll::-webkit-scrollbar,
[class*="scroll"]::-webkit-scrollbar,
body::-webkit-scrollbar {
  display: var(--display);
  width: 12px;
  height: var(--scroll-size);
  background: #3f474d;
} */

.component-frame {
  z-index: 0 !important;
}
/* Boton verde */
.btn-custom {
  background: var(--bg-btn);
  border-radius: 15px;
  color: white;
  border: none;
  padding: 18px 67px;
  font-size: 14px;
}

.btn-custom:hover {
  background: var(--second-color-green);
}

/* Bordes redondeados basicos para los contenedores */
.border-box {
  border-radius: 20px;
  background: #ffffff;
  border: 1px solid #efefef;
}

/* Bordes verdes redondeados para los contenedores */
.border-box-green {
  background: var(--color-white);
  border: 1px solid #ffc107;
  box-sizing: border-box;
  border-radius: 20px;
}

/* Centrar vertical y horizontalemente el spinner u otro elemento */
.center-spinner,
.center-element {
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
}

.center-element {
  color: var(--second-color-gray);
  font-size: 14px;
}

/* Icono triste para "resultados no encontrados" */
.no-result::before {
  font-family: "Font Awesome 5 Free";
  content: "\f119";
  font-size: 96px;
  color: var(--second-color-gray);
}

.cursor-pointer {
  cursor: pointer;
}

/* Animacion esqueloto de pre-carga */
@keyframes load {
  0% {
    background: #ccc;
  }

  50% {
    background: #eee;
  }

  100% {
    background: #ccc;
  }
}

.loader {
  height: 50px;
  animation: load 2s linear infinite alternate;
  border-radius: 30px;
  color: transparent;
}
</style>

