<template>
  <div @click="sidebarChangeVal(false)" v-show="show" class="shadow"></div>
  <transition name="sidebar">
    <div v-show="show" class="sidebar">
      <div @click="sidebarChangeVal(false)" class="xsign">
        <font-awesome-icon icon="fa-solid fa-xmark" />
      </div>
      <div class="logo">
        <img
          src="../../../imgs/homeAssets/yamm_tech_logo.png"
          alt="YammTech Logo"
          style="height: 50px; width: auto"
        />
      </div>
      <p class="head">
        Ready to build something amazing? Let's turn your idea into reality.
      </p>
      <div class="contact">
        <h5>Contact Us</h5>
        <ul>
          <li>
            <font-awesome-icon icon="fa-solid fa-phone" />
            +1 (437) 559-1485
          </li>
          <li>
            <font-awesome-icon icon="fa-solid fa-envelope" />
            info@yammtech.com
          </li>
          <li class="add">
            <font-awesome-icon icon="fa-solid fa-location-dot" />
            <p>Toronto, Canada</p>
          </li>
        </ul>
      </div>
      <div class="subbb">
        <div class="subhead">Subscribe</div>
        <div class="inputgroup mainSubmit">
          <input id="email" type="email" placeholder="example@gmail.com" />
          <button class="mainBtn" id="submitbtn">Send</button>
        </div>
        <p>
          At vero eos et accusamus et iusto odio as part dignissimos ducimus
          blandit.
        </p>
      </div>
      <div class="socials">
        <div class="social">
          <font-awesome-icon icon="fa-brands fa-linkedin-in" />
        </div>
        <div class="social">
          <font-awesome-icon icon="fa-brands fa-x-twitter" />
        </div>
        <div class="social">
          <font-awesome-icon icon="fa-brands fa-youtube" />
        </div>
        <div class="social">
          <font-awesome-icon icon="fa-brands fa-github" />
        </div>
      </div>
    </div>
  </transition>
</template>

<script>
export default {
  props: ["show"],
  methods: {
    sidebarChangeVal(val) {
      this.$store.dispatch("sidebar/sidebarState", val);
      document.querySelector(".bars").classList.remove("sidebaract");
    },
  },
};
</script>

<style lang="scss" scoped>
.sidebar {
  overscroll-behavior: contain;
  width: 500px;
  height: 100vh;
  position: fixed;
  top: 0;
  right: 0;
  overflow-y: auto;
  z-index: 1001;
  background-color: #181818;
  padding: 90px 50px 50px;
  color: #ffffff;
  &::-webkit-scrollbar {
    display: none;
  }
  .xsign {
    position: fixed;
    top: 30px;
    right: 35px;
    border: 2px solid white;
    width: 25px;
    height: 25px;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 50%;
    cursor: pointer;
    transition-duration: 0.3s;
    @media (min-width: 992px) {
      &:hover {
        color: var(--prim-color);
        transform: scale(1.1);
        border-color: var(--prim-color);
      }
    }
  }
  .head {
    padding: 35px 0;
    font-size: 22px;
    line-height: 1.4em;
    color: #fefefe;
    font-weight: 700;
  }
  .contact {
    padding: 35px 0px;
    h5 {
      margin-bottom: 25px;
      font-weight: 600;
    }
    ul {
      li {
        &.add {
          display: flex;
          svg {
            margin-right: 20px;
          }
        }
        color: #fafafab3;
        margin-bottom: 22px;
        font-size: 16px;
        &:last-of-type {
          margin-bottom: 0px;
        }
        svg {
          font-size: 20px;
          margin-right: 10px;
          color: var(--prim-color);
        }
      }
    }
  }
  .subbb {
    padding: 35px 0px;
    .subhead {
      font-size: 20px;
      margin-bottom: 25px;
      font-weight: 700;
      color: #fefefe;
    }
    p {
      margin-top: 25px;
      color: #fefefeb3;
      font-weight: 500;
    }
    .mainBtn {
      padding: 5px 27px;
    }
  }
  .socials {
    padding: 35px 0;
    display: flex;
    align-items: center;
    justify-content: start;
    .social {
      margin: 7px;
      display: flex;
      align-items: center;
      justify-content: center;
      width: 36px;
      height: 36px;
      border-radius: 50%;
      border: 2px solid white;
      cursor: pointer;
      transition-duration: 0.4s;
      &:hover {
        border-color: var(--prim-color);
        transform: scale(1.1);
      }
    }
  }
}

.sidebar-enter-active,
.sidebar-leave-active {
  transition-duration: 0.5s;
}

.sidebar-enter-from,
.sidebar-leave-to {
  opacity: 0;
  transform: translateX(100px);
}
</style>
