<template>
  <header>
    <div class="container">
      <div class="content">
        <div class="logo">
          <router-link
            aria-label="homePage"
            to="/"
            class="logo-link d-flex align-items-center"
          >
            <img
              src="../../../imgs/homeAssets/yamm_tech_logo.png"
              alt="YammTech Logo"
            />
            <span class="logo-text">YAMM <span>TECH</span></span>
          </router-link>
        </div>

        <!-- Desktop Links -->
        <div class="links d-none d-xl-flex">
          <ul>
            <li class="liLinks">
              <router-link class="aLinks" to="/">home</router-link>
            </li>
            <li class="liLinks">
              <router-link class="aLinks" to="/about">who we are</router-link>
            </li>
            <li class="liLinks">
              <router-link class="aLinks" to="/services"
                >what we do</router-link
              >
            </li>
            <li class="liLinks">
              <router-link class="aLinks" to="/portfolio">our work</router-link>
            </li>
            <li class="liLinks">
              <router-link class="aLinks" to="/blog?page=1"
                >digital marketing</router-link
              >
            </li>
            <li class="liLinks">
              <router-link class="aLinks" to="/contact">let's talk</router-link>
            </li>
          </ul>
        </div>

        <!-- Tools Section -->
        <div class="tools">
          <!-- Mobile Bars -->
          <div
            @click="barsclass"
            class="mdbars d-flex d-xl-none"
            data-bs-toggle="collapse"
            href="#mdlinks"
            role="button"
            aria-label="bars"
            aria-expanded="false"
            aria-controls="mdlinks"
          >
            <div class="bar"></div>
          </div>

          <!-- Sidebar Toggle (Desktop) -->
          <div class="d-none d-xl-flex bars" @click="sidebarChangeVal(true)">
            <div class="barcontainer">
              <div class="bar bar1 inbar"></div>
              <div class="bar bar2"></div>
              <div class="bar bar3"></div>
              <div class="bar bar4 outbar"></div>
            </div>
          </div>
        </div>

        <!-- Mobile Menu -->
        <div class="mdlinks d-xl-none collapse" id="mdlinks">
          <ul class="mainul">
            <li>
              <router-link class="aLinks" to="/">home</router-link>
            </li>
            <li>
              <router-link class="aLinks" to="/about">who we are</router-link>
            </li>
            <li>
              <router-link class="aLinks" to="/services"
                >what we do</router-link
              >
            </li>
            <li>
              <router-link class="aLinks" to="/portfolio">our work</router-link>
            </li>
            <li>
              <router-link class="aLinks" to="/blog?page=1"
                >digital marketing</router-link
              >
            </li>
            <li>
              <router-link class="aLinks" to="/contact">let's talk</router-link>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </header>
  <sidebar :show="sidebarval"></sidebar>
</template>

<script>
import sidebar from "../ui/BaseSidebar.vue";

export default {
  data() {
    return {
      // No shop or pages data needed anymore
    };
  },
  methods: {
    headerBg() {
      const body = document.body;
      let lastScroll = 0;

      window.addEventListener("scroll", () => {
        const currentScroll = window.scrollY;

        if (currentScroll <= 115) {
          body.classList.remove("scroll-up");
        }

        if (
          currentScroll > lastScroll &&
          !body.classList.contains("scroll-down") &&
          currentScroll > 115
        ) {
          body.classList.remove("scroll-up");
          body.classList.add("scroll-down");
        }

        if (
          currentScroll < lastScroll &&
          body.classList.contains("scroll-down")
        ) {
          body.classList.remove("scroll-down");
          body.classList.add("scroll-up");
        }

        lastScroll = currentScroll;
      });
    },
    // Removed activeLi and deactiveLi methods - not needed anymore
    sidebarChangeVal(val) {
      document.querySelector(".bars").classList.add("sidebaract");
      this.$store.dispatch("sidebar/sidebarState", val);
    },
    barsclass() {
      document.querySelector(".mdbars").classList.toggle("activebars");
    },
  },
  computed: {
    // Removed pagesLi, shopLi, getCartProducts - not needed
    sidebarval() {
      return this.$store.getters["sidebar/sidebarState"];
    },
  },
  components: {
    sidebar,
  },
  created() {
    this.headerBg();
  },
  watch: {
    $route() {
      // Removed cart icon logic - cart icon removed
      this.headerBg();
    },
  },
};
</script>

<style lang="scss" scoped>
header {
  position: fixed;
  top: 0;
  left: 0;
  z-index: 999;
  width: 100%;
  transition: all 400ms cubic-bezier(0.4, 0, 0.2, 1);
  border-bottom: 1px solid transparent;

  &.scroll-up {
    background: rgba(10, 10, 10, 0.8);
    backdrop-filter: blur(20px);
    -webkit-backdrop-filter: blur(20px);
    border-bottom: 1px solid var(--glass-border);
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
  }

  @media (max-width: 1199px) {
    .content {
      height: 80px !important;
    }
  }

  @media (max-width: 1199px) {
    .content {
      padding-top: 0 !important;
    }
  }

  .content {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding-top: 10px;

    .logo {
      .logo-link {
        text-decoration: none;
        gap: 15px;
        background: rgba(255, 255, 255, 0.03);
        padding: 5px 15px;
        border-radius: 50px;
        backdrop-filter: blur(5px);
        border: 1px solid rgba(255, 255, 255, 0.05);
        transition: all 0.3s ease;

        img {
          height: 42px;
          width: auto;
          filter: drop-shadow(0 0 10px rgba(31, 81, 254, 0.5));
          transition: transform 0.3s ease;
        }

        &:hover {
          background: rgba(255, 255, 255, 0.08);
          border-color: rgba(255, 196, 46, 0.3);
        }

        &:hover img {
          transform: scale(1.08);
          filter: drop-shadow(0 0 15px rgba(255, 196, 46, 0.6));
        }

        .logo-text {
          font-size: 24px;
          font-weight: 800;
          letter-spacing: 1px;
          color: white;
          text-transform: uppercase;
          font-family: "Outfit", sans-serif;

          span {
            color: var(--sec-color);
          }
        }
      }
    }

    .tools {
      display: flex;
      align-items: center;

      .mdbars {
        display: flex;
        align-items: center;
        justify-content: center;
        cursor: pointer;
        width: 30px;
        height: 27px;

        &.activebars {
          .bar {
            transition-duration: 0.3s;
            background-color: transparent;
            &::before {
              transform: rotate(-45deg);
              top: 0px;
            }
            &::after {
              transform: rotate(45deg);
              bottom: 0px;
            }
          }
        }

        .bar {
          width: 30px;
          height: 3px;
          background-color: #ffffff;
          border-radius: 6px;
          position: relative;

          &::before {
            content: "";
            position: absolute;
            width: 30px;
            height: 3px;
            background-color: #ffffff;
            border-radius: 6px;
            top: 8px;
            transition-duration: 0.3s;
          }
          &::after {
            content: "";
            position: absolute;
            width: 30px;
            height: 3px;
            background-color: #ffffff;
            border-radius: 6px;
            bottom: 8px;
            transition-duration: 0.3s;
          }
        }
      }

      .bars {
        border: 2px solid #ffffff;
        border-radius: 50%;
        width: 45px;
        height: 45px;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        cursor: pointer;

        &:hover {
          .inbar {
            transform: translateY(6px) !important;
          }
          .bar2 {
            transform: translateY(6px) !important;
            width: 18px !important;
          }
          .bar3 {
            transform: translateY(6px) !important;
          }
          .bar4 {
            transform: translateY(6px) !important;
            width: 0 !important;
          }
        }

        &.sidebaract {
          .inbar {
            transform: translateY(6px) !important;
          }
          .bar2 {
            transform: translateY(6px) !important;
            width: 18px !important;
          }
          .bar3 {
            transform: translateY(6px) !important;
          }
          .bar4 {
            transform: translateY(6px) !important;
            width: 0 !important;
          }
        }

        .barcontainer {
          overflow: hidden;

          .bar {
            width: 18px;
            height: 2px;
            background-color: #ffffff;
            margin-bottom: 4px;
            border-radius: 6px;
            transition-duration: 0.3s;

            &.bar1,
            &.bar2 {
              width: 14px;
            }
            &.inbar {
              transform: translateY(-5px);
            }
          }
        }
      }
    }

    .links {
      ul {
        display: flex;
        align-items: center;
        margin: 0;
        padding: 0;

        li.liLinks {
          position: relative;
          list-style: none;

          &:not(:last-of-type) {
            margin-right: 40px;
          }

          .aLinks {
            cursor: pointer;
            display: flex;
            align-items: center;
            height: 90px;
            transition: var(--transition);
            color: var(--text-main);
            font-size: 14px;
            text-transform: uppercase;
            font-weight: 500;
            text-decoration: none;
            font-family: var(--font-heading);
            letter-spacing: 1px;
            position: relative;

            &::after {
              content: "";
              position: absolute;
              bottom: 30px;
              left: 50%;
              width: 0;
              height: 2px;
              background-color: var(--sec-color);
              transition: var(--transition);
              transform: translateX(-50%);
              box-shadow: 0 0 10px var(--sec-color);
            }

            &:hover {
              color: var(--sec-color);
              &::after {
                width: 100%;
              }
            }

            &.router-link-active {
              color: var(--sec-color);
              &::after {
                width: 100%;
              }
            }

            svg {
              margin-left: 5px;
            }
          }
        }
      }
    }

    .mdlinks {
      position: absolute;
      top: 80px;
      left: 0px;
      background-color: #181818;
      width: 100%;
      border-bottom: 1px solid rgba(77, 77, 77, 0.3215686275);

      ul.mainul {
        padding: 10px 0;
        max-height: calc(100vh - 80px);
        overflow-y: auto;
        margin: 0;

        li {
          position: relative;
          list-style: none;

          a {
            display: block;
            padding: 8px 20px;
            color: #fefefeb3;
            text-transform: uppercase;
            font-size: 17px;
            font-weight: 400;
            transition: color 0.3s ease-in-out;
            text-decoration: none;

            @media (min-width: 992px) {
              &:hover {
                color: var(--sec-color);
              }
            }
          }
        }
      }
    }
  }
}

.baseListAnimation-enter-active,
.baseListAnimation-leave-active {
  transition-duration: 0.3s;
}

.baseListAnimation-enter-from,
.baseListAnimation-leave-to {
  opacity: 0;
  transform: translateY(20px);
}
</style>
