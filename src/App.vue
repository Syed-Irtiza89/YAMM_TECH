<template>
  <transition name="loadingScreen">
    <div v-if="!doneLoadingVal" class="loading-screen">
      <div class="loader-content">
        <div class="logo-wrapper">
          <img
            src="./../imgs/homeAssets/yamm_tech_logo.png"
            alt="YammTech Logo"
            class="loader-logo"
          />
          <div class="spinner-ring"></div>
          <div class="spinner-ring-outer"></div>
        </div>
        <div class="loader-text">
          <span>YAMM</span>
          <span class="tech">TECH</span>
        </div>
      </div>
    </div>
  </transition>
  <div @click="scrollup" class="arrow-up">
    <font-awesome-icon icon="fa-solid fa-arrow-up" />
  </div>
  <the-header></the-header>
  <div class="routerView-container">
    <router-view @doneloading="doneloading" />
  </div>
  <the-footer></the-footer>
  <error-alert :visible="errorVisible" @dismiss="dismiss"></error-alert>

  <!-- Floating WhatsApp Button -->
  <a
    href="https://wa.me/14375591485"
    target="_blank"
    class="whatsapp-float"
    aria-label="Contact us on WhatsApp"
  >
    <font-awesome-icon icon="fa-brands fa-whatsapp" />
  </a>
</template>

<script>
import TheHeader from "./components/layouts/TheHeader.vue";
import TheFooter from "./components/layouts/TheFooter.vue";

export default {
  data() {
    return {};
  },
  components: {
    TheHeader,
    TheFooter,
  },
  methods: {
    dismiss() {
      this.$store.dispatch("errorHandling", false);
    },
    arrowup() {
      if (window.scrollY > 350) {
        document.querySelector(".arrow-up").classList.add("scrolled");
      } else {
        document.querySelector(".arrow-up").classList.remove("scrolled");
      }
    },
    scrollup() {
      window.scrollTo(0, 0);
    },
    doneloading(val) {
      this.$store.dispatch("doneLoading", val);
    },
    disableScrolling() {
      document.body.classList.add("no-scroll");
    },
    enableScrolling() {
      document.body.classList.remove("no-scroll");
    },
  },
  computed: {
    doneLoadingVal() {
      return this.$store.getters["doneLoading"];
    },
    errorVisible() {
      return this.$store.getters["errorHandling"];
    },
  },
  created() {
    document.addEventListener("scroll", this.arrowup);
  },
  mounted() {
    this.disableScrolling();

    // add local_storage_cart-data-start

    const cartData = window.localStorage.getItem("cartProducts");
    if (cartData) {
      this.$store.dispatch("cart/initCartLocalStorage", JSON.parse(cartData));
    }

    // add local_storage_cart-data-end
    // add local_storage_WishList-data-start

    const WishListData = window.localStorage.getItem("WishListProducts");
    if (WishListData) {
      this.$store.dispatch(
        "cart/initWishListLocalStorage",
        JSON.parse(WishListData)
      );
    }

    // add local_storage_WishList-data-end
  },
  watch: {
    doneLoadingVal(newVal) {
      console.log(newVal);
      if (newVal) {
        this.enableScrolling();
      } else {
        this.disableScrolling();
      }
    },
  },
};
</script>

<style lang="scss">
// Premium Typography & Global Reset
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

:root {
  --prim-color: #1f51fe;
  --prim-gradient: linear-gradient(135deg, #1f51fe 0%, #0d32b3 100%);
  --sec-color: #ffc42e;
  --sec-gradient: linear-gradient(135deg, #ffc42e 0%, #e6a800 100%);
  --bg-dark: #0a0a0a;
  --bg-card: rgba(255, 255, 255, 0.03);
  --glass-bg: rgba(255, 255, 255, 0.05);
  --glass-border: rgba(255, 255, 255, 0.1);
  --text-main: #fefefe;
  --text-muted: rgba(254, 254, 254, 0.7);
  --font-heading: "Outfit", sans-serif;
  --font-body: "Inter", sans-serif;
  --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  --shadow-premium: 0 20px 40px rgba(0, 0, 0, 0.4);
  --shadow-glow: 0 0 20px rgba(31, 81, 254, 0.3);
}

// Global Utilities
.glass-card {
  background: var(--glass-bg);
  backdrop-filter: blur(12px);
  -webkit-backdrop-filter: blur(12px);
  border: 1px solid var(--glass-border);
  border-radius: 20px;
  transition: var(--transition);

  &:hover {
    background: rgba(255, 255, 255, 0.08);
    border-color: rgba(255, 255, 255, 0.2);
    transform: translateY(-5px);
    box-shadow: var(--shadow-premium);
  }
}

.text-gradient {
  background: var(--prim-gradient);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.whatsapp-float {
  position: fixed;
  bottom: 30px;
  left: 30px;
  width: 60px;
  height: 60px;
  background-color: #25d366;
  color: white;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 30px;
  box-shadow: 0 10px 25px rgba(37, 211, 102, 0.3);
  z-index: 999;
  transition: var(--transition);

  &:hover {
    transform: scale(1.1) translateY(-5px);
    box-shadow: 0 15px 30px rgba(37, 211, 102, 0.4);
    color: white;
  }
}

body.no-scroll {
  overflow: hidden;
}
.routerView-container {
  min-height: 100vh;
}
// bootstrap--root-values-start
:root {
  --bs-body-bg: #181818 !important;
}
// bootstrap--root-values-end
// swiper--root-values-start

:root {
  --swiper-pagination-color: black;
  --swiper-pagination-fraction-color: inherit;
  --swiper-pagination-bullet-size: 16px;
  --swiper-pagination-bullet-width: 16px;
  --swiper-pagination-bullet-height: 16px;
  --swiper-pagination-bullet-inactive-color: var(--prim-color);
  --swiper-pagination-bullet-inactive-opacity: 1;
  --swiper-pagination-bullet-opacity: 1;
  --swiper-pagination-bullet-horizontal-gap: 4px;
  --swiper-pagination-bullet-vertical-gap: 10px;
}

.swiper-pagination {
  position: relative !important;
  margin-top: 40px;
  .swiper-pagination-bullet {
    border: 2px solid var(--prim-color);
    transition-duration: 0.5s;
    &.swiper-pagination-bullet-active {
      border: 2px solid var(--prim-color);
      position: relative;
      &::after {
        content: "";
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        background-color: var(--sec-color);
        border-radius: 50%;
      }
    }
  }
}

// swiper--root-values-end
// vue-3-carousel-root-value edited for my Pagination-start
.noUi-touch-area {
  width: 2px;
}
:root {
  --vc-pgn-width: 16px !important;
  --vc-pgn-height: 16px !important;
  --vc-pgn-border-radius: 50% !important;
  --vc-pgn-active-color: #181818 !important;
  --vc-pgn-margin: 0 8px !important;
  --vc-pgn-background-color: var(--sec-color) !important;
}
.carousel__pagination-button {
  &:hover {
    &::after {
      background-color: var(--prim-color) !important;
    }
  }
  &.carousel__pagination-button--active {
    position: relative;
    &:hover {
      &::after {
        background-color: var(--vc-pgn-active-color) !important;
      }
    }
    &::after {
      border: 2px solid var(--prim-color);
    }
    &::before {
      content: "";
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      width: 4px;
      height: 4px;
      border-radius: 50%;
      background-color: var(--sec-color);
    }
  }
}
@media (max-width: 991px) {
  .carousel__pagination {
    margin-top: 35px !important;
  }
}
.carousel__pagination {
  margin-top: 70px;
}

// vue-3-carousel-root-value edited for my Pagination-end
// noUiSlider-override-start

.noUi-target {
  background-color: #4d4d4d !important;
  height: 6px !important;
  border: none !important;
  box-shadow: none !important;
}
.noUi-handle {
  width: 10px !important;
  height: 16px !important;
  right: -5px !important;
  background-color: var(--prim-color) !important;
  box-shadow: none !important;
  border: none !important;
  &::before,
  &::after {
    display: none !important;
  }
}
.noUi-connect {
  background: var(--prim-color) !important;
}

// noUiSlider-override-end
// Variables used in other components
:root {
  --bs-body-bg: #0a0a0a !important;
}

.loading-screen {
  background-color: #071233;
  background: radial-gradient(circle at center, #0a1a4a 0%, #050b1d 100%);
  width: 100%;
  height: 100dvh;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 2000;
  display: flex;
  align-items: center;
  justify-content: center;

  .loader-content {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 30px;
  }

  .logo-wrapper {
    position: relative;
    width: 150px;
    height: 150px;
    display: flex;
    align-items: center;
    justify-content: center;

    .loader-logo {
      width: 80px;
      height: auto;
      z-index: 2;
      filter: drop-shadow(0 0 15px rgba(31, 81, 254, 0.5));
      animation: logoBreath 2s ease-in-out infinite;
    }

    .spinner-ring {
      position: absolute;
      width: 120px;
      height: 120px;
      border: 3px solid transparent;
      border-top: 3px solid var(--prim-color);
      border-radius: 50%;
      animation: spin 1.5s linear infinite;
    }

    .spinner-ring-outer {
      position: absolute;
      width: 140px;
      height: 140px;
      border: 2px solid transparent;
      border-bottom: 2px solid var(--sec-color);
      border-radius: 50%;
      animation: spin 2.5s linear infinite reverse;
      opacity: 0.6;
    }
  }

  .loader-text {
    font-family: var(--font-heading);
    font-size: 24px;
    font-weight: 800;
    letter-spacing: 4px;
    color: white;
    display: flex;
    gap: 10px;
    animation: textFade 2s ease-in-out infinite;

    .tech {
      color: var(--sec-color);
    }
  }
}
body {
  background-color: var(--bg-dark);
  padding: 0;
  margin: 0 !important;
  color: var(--text-main) !important;
  font-family: var(--font-body);
  line-height: 1.6;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  h1,
  h2,
  h3,
  h4,
  h5,
  h6,
  .mainTitle {
    font-family: var(--font-heading);
    font-weight: 700;
  }

  &.scroll-down header {
    transform: translate3d(0, -100%, 0);
    visibility: hidden;
  }
  &.scroll-up header {
    visibility: visible;
  }

  ul {
    list-style: none;
    padding: 0;
    margin: 0;
  }
  a {
    text-decoration: none;
  }
  // css-components-styles-start
  .shadow {
    position: fixed;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    z-index: 1000;
    background-color: rgba(0, 0, 0, 0.6);
  }
  @media (max-width: 991px) {
    .arrow-up {
      right: 15px !important;
    }
  }
  .arrow-up {
    position: fixed;
    bottom: -50px;
    right: 40px;
    z-index: 888;
    &.scrolled {
      bottom: 50px;
    }
    width: 50px;
    height: 50px;
    border-radius: 50%;
    background-color: black;
    display: flex;
    align-items: center;
    justify-content: center;
    transition-duration: 0.4s;
    cursor: pointer;
    svg {
      transition-duration: 0.4s;
      color: var(--prim-color);
      font-size: 22px;
    }
    @media (min-width: 992px) {
      &:hover {
        background-color: var(--sec-color);
        svg {
          color: black;
        }
      }
    }
  }
  // Btns-start
  @media (min-width: 992px) {
    .goToBtn:hover {
      color: var(--prim-color);
      cursor: pointer;
      .hoveranim {
        &::before {
          width: 100%;
        }
      }
    }
  }
  .goToBtn {
    display: flex;
    align-items: center;
    font-size: 17px;
    font-weight: 500;
    width: fit-content;
    color: #fefefe;
    svg {
      margin-left: 15px;
    }
    .hoveranim {
      position: relative;
      transition: color 0.4s;
      & ~ svg {
        transition: color 0.4s;
      }
      &::before {
        content: "";
        position: absolute;
        bottom: -3px;
        left: 0;
        width: 0;
        height: 2px;
        transition-duration: 0.7s;
        transition-timing-function: cubic-bezier(0.47, 1.64, 0.41, 0.8);
        background-color: var(--sec-color);
      }
    }
    &.disabled {
      color: #a9a9a9;
      pointer-events: none;
      user-select: none;
    }
  }
  .myCustomNav {
    .prevbtn,
    .nextbtn {
      margin: 8px;
      width: 60px;
      height: 35px;
      border: 2px solid white;
      cursor: pointer;
      border-radius: 6px;
      background-color: #181818;
      transition-duration: 0.4s;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      @media (min-width: 992px) {
        &:hover {
          background-color: var(--prim-color);
          border-color: var(--prim-color);
        }
      }
      svg {
        color: white;
        font-size: 20px;
      }
    }
  }

  .mainBtn {
    background: var(--sec-gradient);
    border-radius: 12px;
    border: none;
    color: #000000;
    padding: 12px 32px;
    font-size: 16px;
    font-weight: 700;
    position: relative;
    transition: var(--transition);
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    box-shadow: 0 4px 15px rgba(255, 196, 46, 0.2);

    &:hover {
      transform: translateY(-3px);
      box-shadow: 0 8px 25px rgba(255, 196, 46, 0.4);
      color: #000000;
    }

    &:active {
      transform: translateY(-1px);
    }
  }

  .secondBtn {
    background: transparent;
    border: 1px solid rgba(255, 255, 255, 0.2);
    border-radius: 12px;
    color: #ffffff;
    font-size: 16px;
    font-weight: 600;
    transition: var(--transition);
    cursor: pointer;
    padding: 12px 32px;
    display: flex;
    align-items: center;
    justify-content: center;

    &:hover {
      background: rgba(255, 255, 255, 0.05);
      border-color: rgba(255, 255, 255, 0.4);
      transform: translateY(-3px);
      color: white;
    }

    &.lefted {
      margin-left: 20px;
    }
    &.righted {
      margin-right: 20px;
    }
  }
  // Btns-end
  @media (max-width: 991px) {
    .homeheadsec {
      font-size: 14px !important;
      margin-bottom: 12px !important;
    }
  }
  .homeheadsec {
    display: block;
    color: #999696;
    font-size: 16px;
    font-weight: 700;
    margin-bottom: 15px;
    width: fit-content;
    text-transform: capitalize;
    letter-spacing: 1px;
  }
  @media (max-width: 1380px) {
    .mainTitle {
      font-size: 36px !important;
    }
  }
  @media (max-width: 991px) {
    .mainTitle {
      margin-bottom: 15px !important;
      font-size: 28px !important;
    }
  }
  .mainTitle {
    font-size: 42px;
    margin: 0 0 35px;
    color: #fefefe;
    font-weight: 800;
    line-height: 1.2;
  }
  .ourAwards {
    .carousel__slide {
      cursor: pointer;
      justify-content: start;
    }
  }
  .comments {
    ol.carousel__track {
      min-height: 250px;
      position: relative;
    }
  }
  .shape {
    width: 0;
    height: 0;
    border-left: 14px solid var(--sec-color);
    position: absolute;
    filter: drop-shadow(0 0 5px var(--sec-color));
    z-index: 0;
    &:nth-child(1) {
      top: 68%;
      left: 35%;
      animation-name: shapeAnimation1;
      animation-duration: 9s;
      animation-iteration-count: infinite;
      animation-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
    }
    &:nth-child(2) {
      top: 30%;
      left: 72%;
      animation-name: shapeAnimation2;
      animation-duration: 9s;
      animation-iteration-count: infinite;
      animation-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
      animation-delay: -3s;
    }
    &:nth-child(3) {
      top: 25%;
      left: 10%;
      animation-name: shapeAnimation3;
      animation-duration: 9s;
      animation-iteration-count: infinite;
      animation-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
    }
  }
  .mainSubmit {
    background-color: black;
    border-radius: 10px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding-right: 5px;
    @media (max-width: 1199px) and (min-width: 991px) {
      input {
        &::placeholder {
          font-size: 13px !important;
        }
      }
      button {
        padding: 7px 16px !important;
      }
    }
    input {
      width: 100%;
      background-color: black;
      border: none;
      border-top-left-radius: 10px;
      border-bottom-left-radius: 10px;
      padding: 5px 0px 5px 15px;
      height: 50px;
      color: white;
      &:focus {
        outline: none;
      }
      &::placeholder {
        color: #757575;
      }
    }
  }
  .mainP {
    display: block;
    margin-bottom: 30px;
    color: #fefefeb3;
    position: relative;
    font-size: 17px;
    &::after {
      content: "";
      position: absolute;
      bottom: -30px;
      left: 0;
      height: 2px;
      background-color: var(--sec-color);
    }
  }
  .mainInput {
    display: flex;
    flex-direction: column;
    input,
    textarea,
    select {
      background-color: transparent;
      padding: 10px 20px;
      border-radius: 15px;
      border: 2px solid rgb(153, 150, 150);
      margin-bottom: 20px;
      transition-duration: 0.3s;
      &:focus {
        outline: none;
        border-color: var(--prim-color);
      }
    }
    label {
      margin-bottom: 12px;
      color: #fefefeb3;
    }
  }
  .img-container {
    overflow: hidden;
    position: relative;
    &.glasseffect:hover {
      &::after {
        animation: glassEf 1.3s;
      }
    }
    &.glasseffect::after {
      content: "";
      position: absolute;
      top: 0;
      left: -80%;
      width: 50%;
      height: 100%;
      background: linear-gradient(
        to right,
        transparent 0%,
        rgba(255, 255, 255, 0.15) 100%
      );
      z-index: 2;
      transform: skewX(-25deg);
      transition-duration: 0.7s;
    }
  }
  .tags {
    ul {
      display: flex;
      flex-wrap: wrap;
      li {
        font-size: 15px;
        border: 2px solid #fff;
        padding: 3px 15px;
        margin: 5px;
        color: #fefefeb3;
        border-radius: 4px;
        line-height: 1.6rem;
        transition-duration: 0.3s;
        cursor: pointer;
        &:hover {
          background-color: var(--prim-color);
          color: white;
          border-color: var(--prim-color);
        }
      }
    }
  }
  ul.arrowUl {
    @media (max-width: 991px) {
      li {
        margin-bottom: 12px !important;
      }
    }
    li {
      margin-bottom: 20px;
      font-size: 17px;
      color: #fefefeb3;
      cursor: pointer;
      width: fit-content;
      transition-duration: 0.3s;
      &:hover {
        color: var(--prim-color);
      }
      svg {
        margin-right: 5px;
        font-size: 15px;
        color: white;
      }
    }
  }
  .infoBox {
    border: 5px solid #4d4d4d;
    border-radius: 2px;
    padding: 25px 30px 30px;
    display: flex;
    align-items: center;
    flex-direction: column;
    .title {
      width: 100%;
      font-size: 30px;
      margin-bottom: 20px;
      font-weight: 700;
    }
    ul {
      width: 100%;
      margin-bottom: 30px;
      li {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 20px 0;
        border-top: 2px solid #4d4d4d;
        font-size: 17px;
        font-weight: 500;
        &:last-of-type {
          border-bottom: 2px solid #4d4d4d;
        }
      }
    }
  }
  @media (max-width: 991px) {
    .mainPadding {
      margin: 80px 0 !important;
    }
  }
  .mainPadding {
    margin: 150px 0;
  }
  @media (max-width: 991px) {
    .topPaddingO {
      margin-top: 80px !important;
    }
  }
  .topPaddingO {
    margin-top: 150px;
  }
  .swiper-container {
    transform: none;
    overflow-x: hidden;
    position: relative;
  }
  // css-components-end
}

::-webkit-scrollbar {
  width: 12px;
}
::-webkit-scrollbar-thumb {
  background-color: #bbb9b9;
  border-left: 2px solid #464646;
  border-right: 2px solid #464646;
  border-top: 5px solid #464646;
  border-bottom: 5px solid #464646;
  &:hover {
    background-color: #8d8b8b;
  }
}
::-webkit-scrollbar-track {
  background-color: #464646;
  margin: 5px 0;
}
.loadingScreen-enter-active,
.loadingScreen-leave-active {
  transition: opacity 1s ease-out;
}

.loadingScreen-leave-to {
  opacity: 0;
}
@keyframes shapeAnimation1 {
  0% {
    transform: translateX(0) rotate(45deg);
  }
  50% {
    transform: translateX(44px) rotate(90deg);
  }
  100% {
    transform: translateX(0) rotate(45deg);
  }
}
@keyframes shapeAnimation2 {
  0% {
    transform: translateY(0) rotate(0deg);
  }
  50% {
    transform: translateY(25px) rotate(-53deg);
  }
  100% {
    transform: translateY(0) rotate(0deg);
  }
}
@keyframes shapeAnimation3 {
  0% {
    transform: translateY(0) rotate(0deg);
  }
  50% {
    transform: translateY(50px) rotate(-60deg);
  }
  100% {
    transform: translateY(0) rotate(0deg);
  }
}
@keyframes spinner {
  0% {
    transform: translate(-50%, -50%) rotate(0);
  }
  100% {
    transform: translate(-50%, -50%) rotate(360deg);
  }
}
@keyframes spin {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
@keyframes logoBreath {
  0%,
  100% {
    transform: scale(1);
    opacity: 1;
    filter: drop-shadow(0 0 15px rgba(31, 81, 254, 0.5));
  }
  50% {
    transform: scale(1.1);
    opacity: 0.8;
    filter: drop-shadow(0 0 25px rgba(31, 81, 254, 0.8));
  }
}
@keyframes textFade {
  0%,
  100% {
    opacity: 0.5;
    transform: translateY(0);
  }
  50% {
    opacity: 1;
    transform: translateY(-5px);
  }
}
@keyframes glassEf {
  100% {
    left: 125%;
  }
}
</style>
