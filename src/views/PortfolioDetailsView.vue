<template>
  <div class="portfolioDetails">
    <base-hero class="heroBg" :imgUrl="imgUrl">
      <template #head>Portfolio Details</template>
      <template #nav>Portfolio Details</template>
    </base-hero>
    <div class="project-details topPaddingO">
      <div class="container">
        <div v-show="doneLoadingVal" class="img-container">
          <img
            loading="lazy"
            :src="getProjectData.imgUrl"
            alt="portfolio img"
          />
        </div>
        <loading-spinner v-show="!doneLoadingVal"></loading-spinner>
        <div v-if="getProjectData" class="content row">
          <div class="col-lg-6 col-12">
            <div class="homeheadsec">Creative</div>
            <div class="mainTitle">{{ getProjectData.title }}</div>
            <p>{{ getProjectData.paragraph1 }}</p>
            <p>{{ getProjectData.paragraph2 }}</p>
          </div>
          <div class="col-lg-5 offset-lg-1 col-12 seccol">
            <div class="projInfo">Project Info -</div>
            <div class="infoContent row">
              <div class="col-6">
                <div class="dataCont">
                  <div class="infoCat">Category:</div>
                  <div class="infoName">{{ getProjectData.category }}</div>
                </div>
                <div class="dataCont">
                  <div class="infoCat">Software:</div>
                  <div class="infoName">{{ getProjectData.Software }}</div>
                </div>
                <div class="dataCont">
                  <div class="infoCat">Client:</div>
                  <div class="infoName">{{ getProjectData.Client }}</div>
                </div>
              </div>
              <div class="col-6">
                <div class="dataCont">
                  <div class="infoCat">Location:</div>
                  <div class="infoName">{{ getProjectData.location }}</div>
                </div>
                <div class="dataCont">
                  <div class="infoCat">Dated:</div>
                  <div class="infoName">{{ getProjectData.Dated }}</div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <base-meeting :btn="false">
      <template #default>info@yammtech.com</template>
    </base-meeting>
  </div>
</template>
<script>
export default {
  props: ["projectId"],
  data() {
    return {
      imgUrl: require("../../imgs/portfolioDetailsAssets/portfolio_details_bg.webp"),
      doneLoadingVal: false,
    };
  },
  computed: {
    getProjectData() {
      const data = this.$store.getters["portfolio/singleProjectsData"].find(
        (ele) => {
          return ele.id === this.projectId;
        }
      );
      return data ? { ...data } : false;
    },
  },
  methods: {
    doneLoading() {
      const content = document.querySelector(".portfolioDetails .heroBg");
      const imgload = this.$imagesLoaded(content);
      imgload.on("done", () => {
        this.$store.dispatch("doneLoading", true);
      });
    },
    doneImgFetching() {
      const content = document.querySelector(".project-details .img-container");
      const imgload = this.$imagesLoaded(content);
      imgload.on("done", () => {
        this.doneLoadingVal = true;
      });
    },
    async loadData() {
      if (!this.getProjectData) {
        await this.$store.dispatch("portfolio/fetchProjectData", {
          id: this.projectId,
          router: this.$router,
        });
      }
      this.doneLoading();
      this.doneImgFetching();
    },
  },
  async mounted() {
    this.loadData();
  },
};
</script>

<style lang="scss" scoped>
.portfolioDetails {
  background: var(--bg-dark);

  .project-details {
    padding-bottom: 100px;

    .img-container {
      border-radius: 24px;
      overflow: hidden;
      box-shadow: var(--shadow-premium);

      img {
        max-width: 100%;
        max-height: 700px;
        width: 100%;
        object-fit: cover;
        transition: transform 0.8s cubic-bezier(0.4, 0, 0.2, 1);
        &:hover {
          transform: scale(1.02);
        }
      }
    }

    .content {
      margin-top: 80px;

      .mainTitle {
        font-family: var(--font-heading);
        font-size: 48px;
        font-weight: 800;
        color: var(--text-main);
        margin: 15px 0 25px;

        @media (max-width: 991px) {
          font-size: 36px;
        }
      }

      p {
        font-size: 18px;
        line-height: 1.7;
        color: var(--text-muted);
        margin-bottom: 25px;
      }

      .seccol {
        .projInfo {
          font-family: var(--font-heading);
          font-size: 28px;
          font-weight: 800;
          color: var(--text-main);
          margin-bottom: 40px;
          display: flex;
          align-items: center;
          gap: 15px;

          &::after {
            content: "";
            flex: 1;
            height: 1px;
            background: var(--glass-border);
          }
        }

        .dataCont {
          margin-bottom: 30px;

          .infoCat {
            font-family: var(--font-heading);
            color: var(--sec-color);
            font-size: 14px;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 2px;
            margin-bottom: 8px;
          }

          .infoName {
            color: var(--text-main);
            font-size: 18px;
            font-weight: 500;
          }
        }
      }
    }
  }
}
</style>
