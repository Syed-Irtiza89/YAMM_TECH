<template>
  <div class="servicesPage">
    <base-hero class="baseHero" :imgUrl="imgUrl">
      <template #head>what we do</template>
      <template #nav>what we do</template>
    </base-hero>

    <!-- CORE SERVICES - Updated with YammTech services -->
    <div class="coreServices topPaddingO">
      <div class="container">
        <div class="content">
          <div class="head">
            <div class="homeheadsec">our expertise</div>
            <div class="mainTitle">Comprehensive digital solutions</div>
          </div>
          <div class="row">
            <div class="col-xl-5 col-lg-6 col-12">
              <div class="slider-container">
                <div class="imgs-container">
                  <img
                    loading="lazy"
                    data-imgNum="1"
                    class="activeClip"
                    src="../../imgs/servicesAssets/service_7.webp"
                    alt="website development"
                  />
                  <img
                    loading="lazy"
                    data-imgNum="2"
                    class=""
                    src="../../imgs/servicesAssets/service_8.webp"
                    alt="mobile development"
                  />
                  <img
                    loading="lazy"
                    data-imgNum="3"
                    class=""
                    src="../../imgs/servicesAssets/service_9.webp"
                    alt="digital marketing"
                  />
                  <img
                    loading="lazy"
                    data-imgNum="4"
                    class=""
                    src="../../imgs/servicesAssets/service_10.webp"
                    alt="3d rendering"
                  />
                </div>
              </div>
            </div>
            <div class="col-xl-7 col-lg-6 col-12">
              <ul>
                <!-- Service 1: Website Development -->
                <li>
                  <div
                    data-imgNum="1"
                    @mouseenter="hoverCoreServ($event, '1')"
                    :class="['linkcont', { active: activeService === '1' }]"
                  >
                    <div class="info">
                      <div class="servname">Website Development</div>
                      <p>
                        Custom, high-performance websites and web applications
                        built with modern frameworks like React, Vue, and
                        Node.js. From corporate sites to complex enterprise
                        portals, we deliver scalable, secure, and SEO-optimized
                        solutions.
                      </p>
                    </div>
                    <div class="arrowIcon">
                      <font-awesome-icon
                        icon="fa-solid fa-arrow-up-right-from-square"
                      />
                    </div>
                  </div>
                </li>

                <!-- Service 2: Mobile Applications -->
                <li>
                  <div
                    data-imgNum="2"
                    @mouseenter="hoverCoreServ($event, '2')"
                    :class="['linkcont', { active: activeService === '2' }]"
                  >
                    <div class="info">
                      <div class="servname">Mobile Applications</div>
                      <p>
                        Native and cross-platform mobile apps for iOS and
                        Android. We build feature-rich, intuitive applications
                        using Flutter, React Native, and native technologies
                        that users love to engage with.
                      </p>
                    </div>
                    <div class="arrowIcon">
                      <font-awesome-icon
                        icon="fa-solid fa-arrow-up-right-from-square"
                      />
                    </div>
                  </div>
                </li>

                <!-- Service 3: SEO & Digital Marketing -->
                <li>
                  <div
                    data-imgNum="3"
                    @mouseenter="hoverCoreServ($event, '3')"
                    :class="['linkcont', { active: activeService === '3' }]"
                  >
                    <div class="info">
                      <div class="servname">SEO & Digital Marketing</div>
                      <p>
                        Data-driven SEO strategies and digital marketing
                        campaigns that increase visibility, drive qualified
                        traffic, and maximize conversions. From keyword research
                        to content strategy and analytics.
                      </p>
                    </div>
                    <div class="arrowIcon">
                      <font-awesome-icon
                        icon="fa-solid fa-arrow-up-right-from-square"
                      />
                    </div>
                  </div>
                </li>

                <!-- Service 4: 3D Rendering -->
                <li>
                  <div
                    data-imgNum="4"
                    @mouseenter="hoverCoreServ($event, '4')"
                    :class="['linkcont', { active: activeService === '4' }]"
                  >
                    <div class="info">
                      <div class="servname">3D Rendering</div>
                      <p>
                        Photorealistic 3D rendering, architectural
                        visualization, and interactive 3D experiences. We bring
                        concepts to life with stunning visuals for real estate,
                        product design, and immersive web experiences.
                      </p>
                    </div>
                    <div class="arrowIcon">
                      <font-awesome-icon
                        icon="fa-solid fa-arrow-up-right-from-square"
                      />
                    </div>
                  </div>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- CONSULTING SECTION (5th service - Special highlight) -->
    <div class="consultingSection">
      <div class="container">
        <div class="content">
          <div class="row align-items-center">
            <div class="col-lg-6">
              <div class="consulting-badge">Service Highlight</div>
              <div class="mainTitle">Technology Consulting</div>
              <p class="consulting-desc">
                Strategic technology consulting that bridges the gap between
                business goals and technical execution. Our experienced
                consultants help you make informed decisions about architecture,
                stack selection, digital transformation, and technology roadmap
                planning.
              </p>
              <ul class="consulting-list">
                <li>
                  <font-awesome-icon
                    icon="fa-solid fa-check-circle"
                    style="color: #1f51fe"
                  />
                  <span>IT Strategy & Roadmap</span>
                </li>
                <li>
                  <font-awesome-icon
                    icon="fa-solid fa-check-circle"
                    style="color: #1f51fe"
                  />
                  <span>Technology Stack Advisory</span>
                </li>
                <li>
                  <font-awesome-icon
                    icon="fa-solid fa-check-circle"
                    style="color: #1f51fe"
                  />
                  <span>Digital Transformation</span>
                </li>
                <li>
                  <font-awesome-icon
                    icon="fa-solid fa-check-circle"
                    style="color: #1f51fe"
                  />
                  <span>Architecture Review & Optimization</span>
                </li>
              </ul>
            </div>
            <div class="col-lg-6">
              <div class="consulting-image glasseffect">
                <img
                  src="../../imgs/servicesAssets/service_img_1.webp"
                  alt="technology consulting"
                />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- TECH STACK SECTION - Keep but update text -->
    <div class="relatedServices">
      <div class="container">
        <div class="content row">
          <div class="col-xl-5 col-lg-6 col-12">
            <div class="img-container glasseffect">
              <img
                loading="lazy"
                src="../../imgs/servicesAssets/service_img_1.webp"
                alt="technology stack"
              />
            </div>
          </div>
          <div class="col-lg-6 col-12 offset-xl-1">
            <div class="info-container">
              <div class="mainTitle">Technologies we master</div>
              <div class="row">
                <div class="col-md-6 col-12">
                  <ul>
                    <li>
                      <div class="goToBtn">
                        <font-awesome-icon
                          icon="fa-solid fa-arrow-right-long"
                        />
                        <div class="hoveranim">React / Next.js / Vue</div>
                      </div>
                    </li>
                    <li>
                      <div class="goToBtn">
                        <font-awesome-icon
                          icon="fa-solid fa-arrow-right-long"
                        />
                        <div class="hoveranim">Node.js / Python / PHP</div>
                      </div>
                    </li>
                    <li>
                      <div class="goToBtn">
                        <font-awesome-icon
                          icon="fa-solid fa-arrow-right-long"
                        />
                        <div class="hoveranim">
                          Flutter / React Native / Kotlin
                        </div>
                      </div>
                    </li>
                    <li>
                      <div class="goToBtn">
                        <font-awesome-icon
                          icon="fa-solid fa-arrow-right-long"
                        />
                        <div class="hoveranim">AWS / Azure / Google Cloud</div>
                      </div>
                    </li>
                  </ul>
                </div>
                <div class="col-md-6 col-12">
                  <ul>
                    <li>
                      <div class="goToBtn">
                        <font-awesome-icon
                          icon="fa-solid fa-arrow-right-long"
                        />
                        <div class="hoveranim">
                          WordPress / Shopify / Webflow
                        </div>
                      </div>
                    </li>
                    <li>
                      <div class="goToBtn">
                        <font-awesome-icon
                          icon="fa-solid fa-arrow-right-long"
                        />
                        <div class="hoveranim">
                          Blender / Maya / Unreal Engine
                        </div>
                      </div>
                    </li>
                    <li>
                      <div class="goToBtn">
                        <font-awesome-icon
                          icon="fa-solid fa-arrow-right-long"
                        />
                        <div class="hoveranim">
                          Google Analytics / SEMrush / Ahrefs
                        </div>
                      </div>
                    </li>
                    <li>
                      <div class="goToBtn">
                        <font-awesome-icon
                          icon="fa-solid fa-arrow-right-long"
                        />
                        <div class="hoveranim">
                          Docker / Kubernetes / Jenkins
                        </div>
                      </div>
                    </li>
                  </ul>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- DEVELOPMENT APPROACH - With FontAwesome Icons -->
    <div class="approachSection">
      <div class="container">
        <div class="content">
          <div class="head text-center">
            <div class="homeheadsec">our delivery framework</div>
            <div class="mainTitle">How we bring ideas to life</div>
          </div>
          <div class="approach-timeline">
            <div class="timeline-line"></div>
            <div class="row approach-grid">
              <div class="col-lg-3 col-md-6 col-12">
                <div class="approach-card">
                  <div class="approach-icon">
                    <font-awesome-icon icon="fa-solid fa-clipboard-list" />
                  </div>
                  <h3>Discovery & Strategy</h3>
                  <p>
                    We dive deep into your business goals, user needs, and
                    market landscape to define the perfect solution
                    architecture.
                  </p>
                  <div class="approach-tag">1-2 weeks</div>
                </div>
              </div>
              <div class="col-lg-3 col-md-6 col-12">
                <div class="approach-card">
                  <div class="approach-icon">
                    <font-awesome-icon icon="fa-solid fa-pencil-ruler" />
                  </div>
                  <h3>Design & Prototyping</h3>
                  <p>
                    Wireframes, interactive prototypes, and pixel-perfect
                    designs that balance beauty with functionality and user
                    experience.
                  </p>
                  <div class="approach-tag">2-3 weeks</div>
                </div>
              </div>
              <div class="col-lg-3 col-md-6 col-12">
                <div class="approach-card">
                  <div class="approach-icon">
                    <font-awesome-icon icon="fa-solid fa-code" />
                  </div>
                  <h3>Development & Testing</h3>
                  <p>
                    Agile sprints, clean code, continuous integration, and
                    rigorous testing to build robust, scalable systems.
                  </p>
                  <div class="approach-tag">4-12 weeks</div>
                </div>
              </div>
              <div class="col-lg-3 col-md-6 col-12">
                <div class="approach-card">
                  <div class="approach-icon">
                    <font-awesome-icon icon="fa-solid fa-rocket" />
                  </div>
                  <h3>Launch & Optimize</h3>
                  <p>
                    Seamless deployment, performance monitoring, and ongoing
                    optimization to ensure long-term success.
                  </p>
                  <div class="approach-tag">ongoing</div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- CTA SECTION -->
    <base-meeting :btn="true">
      <template #default>
        Ready to start your <br />
        next project?
      </template>
    </base-meeting>
  </div>
</template>

<script>
export default {
  data() {
    return {
      imgUrl: require("../../imgs/servicesAssets/service_hero_bg.webp"),
      activeService: 1,
    };
  },
  methods: {
    hoverCoreServ(e, imgNum) {
      this.activeService = imgNum;
      const imgs = document.querySelectorAll(
        ".slider-container .imgs-container img"
      );
      const container = document.querySelector(
        ".slider-container .imgs-container"
      );
      imgs.forEach((img) => {
        if (img.dataset.imgnum === e.target.dataset.imgnum) {
          if (container.lastChild === img) {
            return;
          }
          img.classList.add("activeClip");
          container.appendChild(img);
          setTimeout(() => {
            img.classList.remove("activeClip");
          }, 1000);
        }
      });
    },
    doneLoading() {
      const content = document.querySelector(".baseHero");
      const imgload = this.$imagesLoaded(content);
      imgload.on("done", () => {
        this.$store.dispatch("doneLoading", true);
      });
    },
  },
  mounted() {
    this.doneLoading();
  },
};
</script>

<style lang="scss" scoped>
.servicesPage {
  .coreServices {
    @media (max-width: 991px) {
      .head {
        margin-bottom: 45px !important;
      }
    }
    .head {
      text-align: center;
      margin-bottom: 90px;
      .homeheadsec {
        width: 100%;
      }
    }
    ul {
      li {
        @media (max-width: 575px) {
          .linkcont {
            flex-direction: column-reverse;
            .arrowIcon {
              margin-right: auto;
              margin-bottom: 20px;
              width: 60px !important;
              height: 60px !important;
            }
          }
        }
        &:nth-child(1) {
          .linkcont {
            padding: 0 0 25px 0;
          }
        }
        .linkcont {
          color: #fefefe;
          display: flex;
          align-items: center;
          justify-content: space-between;
          padding: 25px 0;
          border-bottom: 1px solid #4d4d4d;
          cursor: pointer;
          &.active {
            .arrowIcon {
              background-color: var(--prim-color);
              border: 2px solid var(--prim-color);
              color: white;
            }
          }
          .info {
            max-width: 480px;
            margin-right: 30px;
            .servname {
              font-size: 30px;
              margin-bottom: 15px;
              font-weight: 700;
            }
            p {
              font-size: 17px;
              color: #fefefeb3;
              margin-bottom: 0;
            }
          }
          .arrowIcon {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 80px;
            height: 80px;
            border-radius: 50%;
            color: #999696;
            background-color: transparent;
            border: 2px solid #999696;
            transition-duration: 0.3s;
            svg {
              font-size: 25px;
            }
          }
        }
      }
    }
    .slider-container {
      padding: 0px 20px 20px 0;
      .imgs-container {
        position: relative;
        height: 600px;
        max-width: 416px;
        &::after {
          content: "";
          position: absolute;
          bottom: -20px;
          right: -20px;
          width: 100%;
          height: 100%;
          background-color: var(--prim-color);
          border-radius: 15px;
          z-index: 1;
        }
        img {
          position: absolute;
          top: 0;
          left: 0;
          height: 100%;
          max-width: 100%;
          width: 100%;
          z-index: 2;
          border-radius: 15px;
          object-fit: cover;
          transition: clip-path 1s;
          &.activeClip {
            animation: imgTransAnimation 0.7s;
          }
        }
      }
    }
  }

  // CONSULTING SECTION
  .consultingSection {
    margin-top: 140px;
    margin-bottom: 140px;

    .consulting-badge {
      display: inline-block;
      padding: 5px 15px;
      background-color: rgba(31, 81, 254, 0.15);
      color: #1f51fe;
      border-radius: 30px;
      font-size: 14px;
      font-weight: 600;
      margin-bottom: 20px;
    }

    .mainTitle {
      margin-bottom: 25px !important;
    }

    .consulting-desc {
      color: #fefefeb3;
      font-size: 18px;
      line-height: 1.8;
      margin-bottom: 30px;
    }

    .consulting-list {
      list-style: none;
      padding: 0;

      li {
        display: flex;
        align-items: center;
        margin-bottom: 15px;

        svg {
          font-size: 20px;
          margin-right: 15px;
        }

        span {
          color: #fefefe;
          font-size: 17px;
        }
      }
    }

    .consulting-image {
      border-radius: 15px;
      overflow: hidden;

      img {
        width: 100%;
        height: auto;
      }
    }
  }

  .relatedServices {
    margin-top: 140px;
    .content {
      display: flex;
      align-items: center;
      .img-container {
        border-radius: 15px;
        position: relative;
        overflow: hidden;
        &.glasseffect {
          position: relative;
          &:hover::after {
            animation: glassEf 1.3s;
          }
          &::after {
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
        img {
          position: relative;
          z-index: 1;
          width: 100%;
          max-width: 100%;
        }
      }
      .info-container {
        .mainTitle {
          margin-bottom: 50px !important;
        }
        ul {
          display: flex;
          flex-wrap: wrap;
          flex-direction: column;
          li {
            margin-bottom: 20px;
            width: fit-content;
            svg {
              margin: 0 15px 0 0;
              color: var(--prim-color);
              font-size: 25px;
            }
          }
        }
      }
    }
  }

  // DEVELOPMENT APPROACH SECTION - Updated with FontAwesome
  .approachSection {
    margin-top: 140px;
    position: relative;

    .head {
      margin-bottom: 60px;
    }

    .approach-timeline {
      position: relative;
      .timeline-line {
        position: absolute;
        top: 100px;
        left: 0;
        width: 100%;
        height: 2px;
        background: linear-gradient(
          90deg,
          transparent,
          var(--prim-color),
          transparent
        );
        @media (max-width: 991px) {
          display: none;
        }
      }
    }

    .approach-card {
      background: linear-gradient(267.18deg, #161616 0%, #080808 100%);
      border-radius: 15px;
      padding: 40px 30px;
      position: relative;
      margin-bottom: 30px;
      border: 1px solid rgba(255, 255, 255, 0.05);
      transition: all 0.4s ease;
      height: 100%;

      &:hover {
        transform: translateY(-10px);
        border-color: var(--prim-color);
        box-shadow: 0 20px 40px rgba(31, 81, 254, 0.15);

        .approach-icon {
          background-color: var(--prim-color);
          color: white;
        }
      }

      .approach-icon {
        width: 70px;
        height: 70px;
        border-radius: 50%;
        background-color: rgba(31, 81, 254, 0.1);
        color: var(--prim-color);
        font-size: 32px;
        display: flex;
        align-items: center;
        justify-content: center;
        margin-bottom: 25px;
        transition: all 0.4s ease;

        svg {
          width: 32px;
          height: 32px;
        }
      }

      h3 {
        color: #fefefe;
        font-size: 22px;
        font-weight: 600;
        margin-bottom: 15px;
      }

      p {
        color: #fefefeb3;
        font-size: 16px;
        line-height: 1.7;
        margin-bottom: 25px;
      }

      .approach-tag {
        display: inline-block;
        padding: 5px 15px;
        background-color: rgba(31, 81, 254, 0.15);
        color: var(--prim-color);
        border-radius: 30px;
        font-size: 14px;
        font-weight: 500;
      }
    }
  }
}

@keyframes imgTransAnimation {
  0% {
    clip-path: polygon(100% 0, 100% 0, 100% 100%, 100% 100%);
  }
  100% {
    clip-path: polygon(100% 0, 0 0, 0 100%, 100% 100%);
  }
}

@keyframes glassEf {
  0% {
    left: -80%;
  }
  100% {
    left: 120%;
  }
}
</style>
