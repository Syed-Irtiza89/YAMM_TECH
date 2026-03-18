<template>
  <div class="aboutPage">
    <base-hero class="baseHero" :imgUrl="imgUrl">
      <template #head>about us</template>
      <template #nav>about us</template>
    </base-hero>
    <div class="aboutAgency topPaddingO">
      <div class="container">
        <div class="content row">
          <div class="col-lg-7 col-12 spec-col">
            <div class="info">
              <div class="homeheadsec">about us</div>
              <div class="mainTitle">
                About YammTech – Your Partner in <br />
                Digital Success
              </div>
              <p class="mainP">
                We’re YammTech — a passionate software development and digital
                marketing agency helping companies of all sizes win online.
                Whether you need standout UI/UX design, a high-converting
                website, a next-level mobile app, smarter SEO, fintech tools,
                AI-powered videos, or lifelike 3D interior renderings, we’ve got
                you covered.
              </p>
              <p class="mainP">
                Every business is different, so we listen first — then deliver
                tailored digital solutions that boost efficiency, visibility,
                and revenue. Creativity + modern tech + real data = results you
                can measure.
              </p>
            </div>
          </div>
          <div class="col-lg-5 col-12">
            <div class="img-container">
              <img
                loading="lazy"
                src="../../imgs/aboutAssets/about_img_1.webp"
                alt="client"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="whyChooseUs">
      <div class="container">
        <div class="content row">
          <div class="col-xl-5 col-lg-6 col-12">
            <div class="imgcontent">
              <div class="img-container">
                <img
                  loading="lazy"
                  src="../../imgs/aboutAssets/about_img_4.webp"
                  alt="client"
                />
              </div>
            </div>
          </div>
          <div class="col-xl-5 col-lg-6 offset-xl-1 offset-0 col-12">
            <div class="homeheadsec">Our Vision</div>
            <div class="mainTitle">Global technology partner</div>
            <p>
              To be the go-to global technology partner known for innovation,
              dependability, and consistent business growth.
            </p>
            <div class="homeheadsec mt-5">Our Mission</div>
            <div class="mainTitle">Competing – and winning</div>
            <p>
              Deliver secure, scalable, high-performance digital products and
              strategies that help companies compete — and win — in today’s
              fast-moving world.
            </p>
          </div>
        </div>
      </div>
    </div>
    <base-meeting :btn="true">
      <template #default>
        Let’s discuss make <br />
        something cool together
      </template>
    </base-meeting>
  </div>
</template>

<script>
export default {
  data() {
    return {
      imgUrl: require("../../imgs/aboutAssets/about_hero_bg.webp"),
    };
  },
  methods: {
    gsapAnimation() {
      const mm1 = this.$gsap.matchMedia();

      mm1.add(
        {
          mobile: "(max-width: 575px)",
          desktop: "(min-width: 768px)",
        },
        (context) => {
          let { mobile } = context.conditions;

          const tl1 = this.$gsap.timeline({
            scrollTrigger: {
              trigger: ".whyChooseUs .imgcontent",
              start: "bottom bottom",
              end: "bottom center",
              scrub: false,
              markers: false,
              ease: "power4.inOut",
              toggleActions: "play none none reverse",
            },
          });

          tl1.from(
            ".whyChooseUs .imgcontent img",
            {
              bottom: mobile ? -30 : -60,
              right: mobile ? -30 : -60,
              duration: 0.6,
            },
            0
          );
        }
      );
    },
    doneLoading() {
      const content = document.querySelector(".baseHero");
      const imgload = this.$imagesLoaded(content);

      imgload.on("done", () => {
        this.$store.dispatch("doneLoading", true);
        this.$nextTick(() => {
          this.$ScrollTrigger.refresh();
        });
      });
    },
  },
  mounted() {
    this.gsapAnimation();
    this.doneLoading();
  },
  beforeRouteUpdate() {
    this.gsapAnimation();
  },
};
</script>

<style lang="scss" scoped>
.aboutPage {
  background: var(--bg-dark);

  .aboutAgency {
    padding-bottom: 80px;

    .content {
      align-items: center;

      .info {
        .mainTitle {
          font-family: var(--font-heading);
          font-size: 52px;
          line-height: 1.1;
          font-weight: 800;
          color: var(--text-main);
          margin: 15px 0 30px;

          @media (max-width: 991px) {
            font-size: 38px;
          }
        }

        .mainP {
          font-size: 18px;
          color: var(--text-muted);
          line-height: 1.7;
          margin-bottom: 25px;
        }
      }

      .img-container {
        border-radius: 24px;
        overflow: hidden;
        box-shadow: var(--shadow-premium);
        position: relative;

        &::after {
          content: "";
          position: absolute;
          inset: 0;
          border: 1px solid var(--glass-border);
          border-radius: 24px;
          pointer-events: none;
        }

        img {
          width: 100%;
          transition: transform 0.6s cubic-bezier(0.4, 0, 0.2, 1);
          &:hover {
            transform: scale(1.05);
          }
        }
      }
    }
  }

  .whyChooseUs {
    margin-top: 150px;
    padding-bottom: 100px;

    @media (max-width: 991px) {
      margin-top: 80px;
    }

    .mainTitle {
      font-family: var(--font-heading);
      font-size: 36px;
      font-weight: 700;
      color: var(--text-main);
      margin: 10px 0 20px;
    }

    p {
      font-size: 17px;
      line-height: 1.7;
      color: var(--text-muted);
      margin-bottom: 30px;
    }

    .imgcontent {
      padding: 0 40px 40px 0;

      .img-container {
        position: relative;

        &::after {
          content: "";
          position: absolute;
          bottom: -40px;
          right: -40px;
          width: 100%;
          height: 100%;
          background: var(--sec-gradient);
          border-radius: 20px;
          opacity: 0.2;
          z-index: 1;
        }

        img {
          position: relative;
          z-index: 2;
          border-radius: 20px;
          box-shadow: var(--shadow-premium);
          width: 100%;
        }
      }
    }
  }
}
</style>
