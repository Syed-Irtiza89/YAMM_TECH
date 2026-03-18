<template>
  <div class="ourTeamPage">
    <base-hero class="baseHero" :imgUrl="imgUrl">
      <template #head>Our Team</template>
      <template #nav>TEAM</template>
    </base-hero>
    <div class="content topPaddingO">
      <div class="container">
        <div class="head">
          <div class="homeheadsec">Our Team</div>
          <h2 class="mainTitle">Awesome team members</h2>
        </div>
        <div v-show="doneLoadingVal" class="teamGrid row gy-4">
          <div
            v-for="(member, index) in newTeamMembers"
            :key="index"
            class="col-lg-3 col-md-4 col-sm-6 col-12"
          >
            <div class="memberCard text-center">
              <div class="name">{{ member.name }}</div>
              <div class="expertise">{{ member.expertise }}</div>
              <div class="socials mt-3 justify-content-center">
                <div class="social">
                  <font-awesome-icon icon="fa-brands fa-linkedin-in" />
                </div>
                <div class="social">
                  <font-awesome-icon icon="fa-brands fa-github" />
                </div>
              </div>
            </div>
          </div>
        </div>
        <loading-spinner v-show="!doneLoadingVal"></loading-spinner>
      </div>
    </div>
    <base-meeting :btn="true">
      <template #default>
        Let’s disscuse make <br />
        something cool together
      </template>
    </base-meeting>
  </div>
</template>

<script>
export default {
  data() {
    return {
      imgUrl: require("../../../imgs/pages/ourTeam/team_hero_bg.webp"),
      doneLoadingVal: true,
      newTeamMembers: [
        { name: "Minhal", expertise: "Lead Frontend Developer" },
        { name: "Abuzar", expertise: "Senior Backend Developer" },
        { name: "Muhammad", expertise: "Full Stack Engineer" },
        { name: "Moosa", expertise: "Creative UI/UX Designer" },
        { name: "Murtaza", expertise: "Mobile App Specialist" },
        { name: "Ali", expertise: "Digital Marketing & SEO Expert" },
        { name: "Irtiza", expertise: "Project Manager & Strategy" },
      ],
    };
  },
  methods: {
    doneLoading() {
      const content = document.querySelector(".ourTeamPage");
      const imgload = this.$imagesLoaded(content);
      imgload.on("done", () => {
        this.$store.dispatch("doneLoading", true);
      });
    },
    doneImgFetching() {
      const content = document.querySelector(".baseHero");
      const imgload = this.$imagesLoaded(content);
      imgload.on("done", () => {
        this.doneLoadingVal = true;
      });
    },
    async loadData() {
      const data = this.$store.getters["teamMembers/teamData"];
      if (data.length !== 4) {
        await this.$store.dispatch("teamMembers/fetchTeammembersData");
      }
      if (this.getTeamMembersData.length === 0) {
        this.doneLoadingVal = false;
      } else {
        this.doneImgFetching();
      }
    },
  },
  computed: {
    getTeamMembersData() {
      const teamMembersData = this.$store.getters["teamMembers/teamData"];
      return teamMembersData;
    },
  },
  mounted() {
    this.doneLoading();
    this.loadData();
  },
};
</script>

<style lang="scss" scoped>
.ourTeamPage {
  .content {
    @media (max-width: 991px) {
      .head {
        margin-bottom: 45px !important;
      }
    }
    .head {
      text-align: center;
      margin-bottom: 90px;
      .homeheadsec {
        margin: 0px auto 20px;
      }
    }
    .teamGrid {
      padding: 20px 0;
      .memberCard {
        background: rgba(255, 255, 255, 0.03);
        backdrop-filter: blur(10px);
        border: 1px solid rgba(255, 255, 255, 0.08);
        border-radius: 20px;
        padding: 40px 20px;
        transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        height: 100%;
        min-height: 220px;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        position: relative;

        &:hover {
          background: rgba(255, 255, 255, 0.07);
          border-color: var(--prim-color);
          transform: translateY(-10px);
          box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);

          .name {
            color: var(--prim-color);
          }
        }

        .name {
          font-family: var(--font-heading);
          font-size: 24px;
          font-weight: 800;
          color: #fff;
          margin-bottom: 8px;
          transition: color 0.3s ease;
        }

        .expertise {
          color: rgba(255, 255, 255, 0.6);
          font-size: 13px;
          text-transform: uppercase;
          letter-spacing: 1.5px;
          font-weight: 600;
          margin-bottom: 20px;
        }

        .socials {
          display: flex;
          gap: 12px;
          .social {
            width: 36px;
            height: 36px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #fff;
            font-size: 14px;
            transition: all 0.3s ease;
            &:hover {
              background: var(--prim-color);
              color: #000;
            }
          }
        }
      }
    }
  }
}
</style>
