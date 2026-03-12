<template>
  <div class="portfolioPage">
    <base-hero class="baseHero" :imgUrl="imgUrl">
      <template #head>our work</template>
      <template #nav>our work</template>
    </base-hero>

    <!-- RECENT WORK SECTION - Upgraded -->
    <div class="recentWork topPaddingO">
      <div class="container">
        <div class="content">
          <div class="head-container">
            <div class="info">
              <div class="homeheadsec">our portfolio</div>
              <div class="mainTitle">Featured projects</div>
            </div>
            <div class="carousel-controls">
              <ul>
                <li
                  data-sort="*"
                  :class="{ active: activeSort === '*' }"
                  @click="activeField('*')"
                >
                  all
                </li>
                <li
                  data-sort=".web-development"
                  :class="{ active: activeSort === '.web-development' }"
                  @click="activeField('.web-development')"
                >
                  web development
                </li>
                <li
                  data-sort=".mobile-apps"
                  :class="{ active: activeSort === '.mobile-apps' }"
                  @click="activeField('.mobile-apps')"
                >
                  mobile apps
                </li>
                <li
                  data-sort=".cloud-solutions"
                  :class="{ active: activeSort === '.cloud-solutions' }"
                  @click="activeField('.cloud-solutions')"
                >
                  cloud solutions
                </li>
                <li
                  data-sort=".ai-ml"
                  :class="{ active: activeSort === '.ai-ml' }"
                  @click="activeField('.ai-ml')"
                >
                  AI & ML
                </li>
              </ul>
            </div>
          </div>
          <div ref="isotopeContainer" class="isoContent grid row">
            <div class="grid-sizer"></div>

            <!-- Web Development Projects -->
            <div
              class="img-container isotope-item web-development col-md-4 col-12"
            >
              <router-link aria-label="project" to="/portfolioDetails/1">
                <div class="content">
                  <img
                    src="../../imgs/portfolioAssets/portfolio_9.webp"
                    alt="E-Commerce Platform"
                  />
                  <span>E-Commerce Platform</span>
                  <span>View Case Study</span>
                  <div class="artWork"></div>
                </div>
              </router-link>
            </div>

            <!-- Mobile Apps Projects -->
            <div class="img-container isotope-item mobile-apps col-md-4 col-12">
              <router-link aria-label="project" to="/portfolioDetails/2">
                <div class="content">
                  <img
                    src="../../imgs/portfolioAssets/portfolio_2.webp"
                    alt="Ride Sharing App"
                  />
                  <span>Ride Sharing App</span>
                  <span>View Case Study</span>
                  <div class="artWork"></div>
                </div>
              </router-link>
            </div>

            <!-- Cloud Solutions Projects -->
            <div
              class="img-container isotope-item cloud-solutions col-md-4 col-12"
            >
              <router-link aria-label="project" to="/portfolioDetails/3">
                <div class="content">
                  <img
                    src="../../imgs/portfolioAssets/portfolio_3.webp"
                    alt="Cloud Migration"
                  />
                  <span>Cloud Migration</span>
                  <span>View Case Study</span>
                  <div class="artWork"></div>
                </div>
              </router-link>
            </div>

            <!-- AI/ML Projects - Wide -->
            <div
              class="img-container grid-item--width2 isotope-item ai-ml col-md-4 col-12"
            >
              <router-link aria-label="project" to="/portfolioDetails/4">
                <div class="content">
                  <img
                    src="../../imgs/portfolioAssets/portfolio_7.webp"
                    alt="AI Chatbot Platform"
                  />
                  <span>AI Chatbot Platform</span>
                  <span>View Case Study</span>
                  <div class="artWork"></div>
                </div>
              </router-link>
            </div>

            <!-- Web Development Project -->
            <div
              class="img-container isotope-item web-development col-md-4 col-12"
            >
              <router-link aria-label="project" to="/portfolioDetails/5">
                <div class="content">
                  <img
                    src="../../imgs/portfolioAssets/portfolio_4.webp"
                    alt="CRM System"
                  />
                  <span>CRM System</span>
                  <span>View Case Study</span>
                  <div class="artWork"></div>
                </div>
              </router-link>
            </div>

            <!-- Mobile App Project -->
            <div class="img-container isotope-item mobile-apps col-md-4 col-12">
              <router-link aria-label="project" to="/portfolioDetails/6">
                <div class="content">
                  <img
                    src="../../imgs/portfolioAssets/portfolio_1.webp"
                    alt="Fitness Tracker"
                  />
                  <span>Fitness Tracker</span>
                  <span>View Case Study</span>
                  <div class="artWork"></div>
                </div>
              </router-link>
            </div>

            <!-- Web Development - Wide -->
            <div
              class="img-container grid-item--width2 isotope-item web-development col-md-4 col-12"
            >
              <router-link aria-label="project" to="/portfolioDetails/7">
                <div class="content">
                  <img
                    src="../../imgs/portfolioAssets/portfolio_10.webp"
                    alt="Banking Portal"
                  />
                  <span>Banking Portal</span>
                  <span>View Case Study</span>
                  <div class="artWork"></div>
                </div>
              </router-link>
            </div>
          </div>

          <!-- View All Button -->
          <div class="text-center mt-5">
            <router-link to="/portfolio" class="view-all-btn goToBtn">
              <div class="hoveranim">Load More Projects</div>
              <font-awesome-icon icon="fa-solid fa-arrow-right-long" />
            </router-link>
          </div>
        </div>
      </div>
    </div>

    <!-- NEW SECTION 1: PROJECT STATS / IMPACT -->
    <div class="projectImpact">
      <div class="container">
        <div class="content">
          <div class="head text-center">
            <div class="homeheadsec">by the numbers</div>
            <div class="mainTitle">Our project impact</div>
          </div>
          <div class="impact-grid">
            <div class="impact-item">
              <div class="impact-icon">🚀</div>
              <div class="impact-value">45+</div>
              <div class="impact-label">Projects Delivered</div>
              <div class="impact-desc">Across 6 countries</div>
            </div>
            <div class="impact-item">
              <div class="impact-icon">⏱️</div>
              <div class="impact-value">98%</div>
              <div class="impact-label">On-Time Delivery</div>
              <div class="impact-desc">Average 2 weeks early</div>
            </div>
            <div class="impact-item">
              <div class="impact-icon">💰</div>
              <div class="impact-value">$5.2M</div>
              <div class="impact-label">Client Revenue Generated</div>
              <div class="impact-desc">In first year post-launch</div>
            </div>
            <div class="impact-item">
              <div class="impact-icon">👥</div>
              <div class="impact-value">2.5M+</div>
              <div class="impact-label">Active Users</div>
              <div class="impact-desc">Across all platforms</div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- NEW SECTION 2: CASE STUDIES / TESTIMONIALS -->
    <div class="caseStudies">
      <div class="container">
        <div class="content">
          <div class="head text-center">
            <div class="homeheadsec">client success</div>
            <div class="mainTitle">What our clients say</div>
          </div>
          <div class="row">
            <div class="col-lg-4 col-md-6 col-12">
              <div class="testimonial-card">
                <div class="quote-icon">"</div>
                <p class="testimonial-text">
                  YammTech transformed our legacy system into a modern, scalable
                  platform. Traffic increased 300% with zero downtime.
                </p>
                <div class="client-info">
                  <div class="client-name">Sarah Johnson</div>
                  <div class="client-role">CTO, TechCorp</div>
                </div>
                <div class="project-tag">E-Commerce Platform</div>
              </div>
            </div>
            <div class="col-lg-4 col-md-6 col-12">
              <div class="testimonial-card">
                <div class="quote-icon">"</div>
                <p class="testimonial-text">
                  The mobile app they built for us has 4.8 stars on App Store.
                  User engagement increased by 150% in 3 months.
                </p>
                <div class="client-info">
                  <div class="client-name">Michael Chen</div>
                  <div class="client-role">Founder, FitLife</div>
                </div>
                <div class="project-tag">Fitness App</div>
              </div>
            </div>
            <div class="col-lg-4 col-md-6 col-12">
              <div class="testimonial-card">
                <div class="quote-icon">"</div>
                <p class="testimonial-text">
                  Their AI solution automated 80% of our manual processes. ROI
                  achieved in just 4 months. Highly recommended!
                </p>
                <div class="client-info">
                  <div class="client-name">Priya Patel</div>
                  <div class="client-role">COO, FinServe</div>
                </div>
                <div class="project-tag">AI Automation</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- CTA SECTION -->
    <base-meeting :btn="true">
      <template #default>
        Ready to build your next <br />
        success story?
      </template>
    </base-meeting>
  </div>
</template>

<script>
import Isotope from "isotope-layout";

export default {
  data() {
    return {
      activeSort: "*",
      imgUrl: require("../../imgs/portfolioAssets/portfolio_hero_bg.webp"),
    };
  },
  methods: {
    activeField(sort) {
      this.activeSort = sort;
      if (this.isotope) {
        this.isotope.arrange({ filter: sort });
      }
      this.$ScrollTrigger.refresh();
    },
    initIsotope() {
      const container = this.$refs.isotopeContainer;

      this.isotope = new Isotope(container, {
        itemSelector: ".isotope-item",
        layoutMode: "masonry",
      });
    },
    doneLoading() {
      const content = document.querySelector(".baseHero");
      const imgload = this.$imagesLoaded(content);

      imgload.on("done", () => {
        this.$store.dispatch("doneLoading", true);
        this.$nextTick(() => {
          this.initIsotope();
        });
      });
    },
  },
  mounted() {
    this.doneLoading();
  },
};
</script>

<style lang="scss" scoped>
.portfolioPage {
  .recentWork {
    @media (max-width: 991px) {
      .head-container {
        flex-direction: column;
      }
    }
    .head-container {
      display: flex;
      justify-content: space-between;
      .info {
        .mainTitle {
          margin-bottom: 0 !important;
        }
      }
      .carousel-controls {
        display: flex;
        align-items: flex-end;
        @media (max-width: 991px) {
          ul {
            margin: 20px 0 15px;
          }
        }
        @media (max-width: 575px) {
          ul {
            border-bottom: none !important;
          }
        }
        ul {
          display: flex;
          border-bottom: 1px solid #999696;
          flex-wrap: wrap;
          li {
            margin: 10px 28px 10px 0;
            text-transform: capitalize;
            font-size: 17px;
            color: #fefefeb3;
            cursor: pointer;
            position: relative;
            &::after {
              content: "";
              position: absolute;
              left: 50%;
              bottom: -15px;
              transform: translateX(-50%) scale(0);
              width: 10px;
              height: 10px;
              border-radius: 50%;
              background-color: var(--prim-color);
              transition-duration: 0.5s;
            }
            &:last-of-type {
              margin-right: 0;
            }
            &.active {
              color: var(--prim-color);
              &::after {
                transform: translateX(-50%) scale(1);
              }
            }
          }
        }
      }
    }
    @media (max-width: 991px) {
      .isoContent {
        min-height: 900px;
        margin-top: 15px !important;
      }
    }
    .isoContent {
      margin-top: 90px;
      .img-container {
        margin-bottom: 25px;
        &.grid-item--width2 {
          .content {
            span {
              left: 5% !important;
            }
          }
        }
        .content {
          position: relative;
          overflow: hidden;
          border-radius: 15px;
          width: 100%;
          height: 100%;
          color: #fefefe;
          cursor: pointer;
          &::after {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: transparent;
            transition-duration: 0.3s;
            z-index: 3;
          }
          @media (min-width: 992px) {
            &:hover {
              &::after {
                background-color: rgba(22, 22, 22, 0.4);
              }
              .artWork {
                bottom: -60px;
                left: -40px;
                opacity: 1;
              }
              span:nth-of-type(1),
              span:nth-of-type(2) {
                bottom: 22%;
                opacity: 1;
              }
            }
          }
          img {
            max-width: 100%;
            width: 100%;
            border-radius: 15px;
          }
          span {
            position: absolute;
            display: block;
            text-align: start;
            transition-duration: 0.5s;
            z-index: 5;
            left: 10%;
            opacity: 0;
            color: #fefefe;
            &:nth-of-type(1) {
              bottom: 15%;
              font-size: 22px;
              margin-bottom: 5px;
              font-weight: 700;
            }
            &:nth-of-type(2) {
              transition-delay: 0.1s;
              bottom: 17%;
              color: #fefefeb3;
              font-weight: 500;
              position: relative;
              width: fit-content;
              &::after {
                content: "";
                position: absolute;
                bottom: 8px;
                right: -30px;
                width: 20px;
                height: 1px;
                background-color: #fefefeb3;
              }
            }
          }
          .artWork {
            position: absolute;
            bottom: -100px;
            left: -80px;
            width: 300px;
            height: 300px;
            padding: 105px 20px 80px 65px;
            border-radius: 50%;
            background-color: var(--prim-color);
            z-index: 4;
            opacity: 0;
            transition-duration: 0.5s;
            display: flex;
            flex-direction: column;
            @media (max-width: 1380px) {
              span:nth-child(1) {
                font-size: 20px !important;
              }
            }
          }
        }
      }
    }
  }

  // NEW SECTION 1: Project Impact
  .projectImpact {
    margin-top: 140px;
    margin-bottom: 140px;

    .impact-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 30px;
      margin-top: 60px;

      @media (max-width: 991px) {
        grid-template-columns: repeat(2, 1fr);
      }

      @media (max-width: 575px) {
        grid-template-columns: 1fr;
      }

      .impact-item {
        background: linear-gradient(267.18deg, #161616 0%, #080808 100%);
        border-radius: 15px;
        padding: 40px 30px;
        text-align: center;
        border: 1px solid rgba(255, 255, 255, 0.05);
        transition: all 0.4s ease;

        &:hover {
          transform: translateY(-10px);
          border-color: var(--prim-color);
          box-shadow: 0 20px 40px rgba(255, 74, 23, 0.15);

          .impact-icon {
            transform: scale(1.2);
            color: var(--prim-color);
          }
        }

        .impact-icon {
          font-size: 48px;
          margin-bottom: 20px;
          transition: all 0.3s ease;
        }

        .impact-value {
          color: var(--prim-color);
          font-size: 42px;
          font-weight: 700;
          margin-bottom: 10px;
        }

        .impact-label {
          color: #fefefe;
          font-size: 18px;
          font-weight: 600;
          margin-bottom: 10px;
        }

        .impact-desc {
          color: #fefefeb3;
          font-size: 15px;
        }
      }
    }
  }

  // NEW SECTION 2: Case Studies / Testimonials
  .caseStudies {
    margin-top: 140px;
    margin-bottom: 140px;

    .testimonial-card {
      background: linear-gradient(267.18deg, #161616 0%, #080808 100%);
      border-radius: 15px;
      padding: 40px 30px;
      margin-bottom: 30px;
      position: relative;
      border: 1px solid rgba(255, 255, 255, 0.05);
      transition: all 0.3s ease;

      &:hover {
        transform: translateY(-5px);
        border-color: var(--prim-color);
        box-shadow: 0 15px 30px rgba(255, 74, 23, 0.1);
      }

      .quote-icon {
        color: var(--prim-color);
        font-size: 60px;
        font-family: serif;
        line-height: 1;
        margin-bottom: 10px;
        opacity: 0.3;
      }

      .testimonial-text {
        color: #fefefe;
        font-size: 16px;
        line-height: 1.8;
        margin-bottom: 25px;
        font-style: italic;
      }

      .client-info {
        margin-bottom: 15px;

        .client-name {
          color: #fefefe;
          font-size: 18px;
          font-weight: 600;
        }

        .client-role {
          color: #fefefeb3;
          font-size: 14px;
        }
      }

      .project-tag {
        display: inline-block;
        padding: 5px 15px;
        background-color: rgba(255, 74, 23, 0.15);
        color: var(--prim-color);
        border-radius: 30px;
        font-size: 13px;
        font-weight: 500;
      }
    }
  }
}

// isotope-styling-start
@media (max-width: 991px) {
  .isotope-item,
  .grid-item--width2 {
    width: calc(100% / 2) !important;
  }
}
@media (max-width: 767px) {
  .isotope-item,
  .grid-item--width2 {
    width: 100% !important;
  }
}
.isotope-item {
  width: calc(100% / 3);
  height: 465px;
  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
}
.grid-item--width2 {
  width: calc((100% / 3) * 2);
}
// isotope-styling-end

.view-all-btn {
  display: inline-flex;
  align-items: center;
  padding: 15px 40px;
  background: transparent;
  border: 2px solid var(--prim-color);
  border-radius: 50px;
  color: #fefefe;
  font-size: 16px;
  font-weight: 500;
  transition: all 0.3s ease;

  &:hover {
    background-color: var(--prim-color);
    color: white;
    transform: translateX(5px);
  }

  svg {
    margin-left: 10px;
  }
}
</style>
