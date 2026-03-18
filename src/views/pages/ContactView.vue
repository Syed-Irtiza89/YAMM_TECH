<template>
  <div class="contactPage">
    <base-hero class="baseHero" :imgUrl="imgUrl">
      <template #head>contact us</template>
      <template #nav>contact</template>
    </base-hero>
    <div class="content topPaddingO">
      <div class="container">
        <div class="row align-items-center">
          <div class="col-lg-5">
            <div class="head">
              <div class="homeheadsec">Get Your Free Quote Today</div>
              <h1 class="mainTitle">
                Let’s Build Something <br />
                Amazing Together
              </h1>
            </div>
            <div class="info">
              <p class="mainP">
                Ready to take your business to the next level? Our team of
                experts is here to help you build high-performance digital
                solutions that scale. Fill out the form or reach out directly.
              </p>

              <ul class="contact-details">
                <li>
                  <div class="icon-box">
                    <font-awesome-icon icon="fa-solid fa-phone" />
                  </div>
                  <div class="text">
                    <span>Call Us</span>
                    <p>+1 (437) 559-1485</p>
                  </div>
                </li>
                <li>
                  <div class="icon-box">
                    <font-awesome-icon icon="fa-solid fa-envelope" />
                  </div>
                  <div class="text">
                    <span>Email Us</span>
                    <p>info@yammtech.com</p>
                  </div>
                </li>
                <li>
                  <div class="icon-box">
                    <font-awesome-icon icon="fa-solid fa-location-dot" />
                  </div>
                  <div class="text">
                    <span>Visit Us</span>
                    <p>Toronto, Canada</p>
                  </div>
                </li>
              </ul>

              <div class="whatsapp-box mt-4">
                <a
                  href="https://wa.me/14375591485"
                  target="_blank"
                  class="whatsapp-btn"
                >
                  <font-awesome-icon icon="fa-brands fa-whatsapp" />
                  <span>Chat on WhatsApp</span>
                </a>
              </div>
            </div>
          </div>

          <div class="col-lg-7">
            <div class="glass-card contact-form-wrapper p-4 p-md-5">
              <form action="#" @submit.prevent>
                <div class="row">
                  <div class="col-md-6">
                    <div class="mainInput">
                      <label for="name">Full Name</label>
                      <input
                        id="name"
                        type="text"
                        placeholder="John Doe"
                        required
                      />
                    </div>
                  </div>
                  <div class="col-md-6">
                    <div class="mainInput">
                      <label for="email">Email Address</label>
                      <input
                        id="email"
                        type="email"
                        placeholder="john@example.com"
                        required
                      />
                    </div>
                  </div>
                  <div class="col-md-6">
                    <div class="mainInput">
                      <label for="Mobile">Phone Number</label>
                      <input id="Mobile" type="tel" placeholder="+1..." />
                    </div>
                  </div>
                  <div class="col-md-6">
                    <div class="mainInput">
                      <label for="ProjectType">Service Needed</label>
                      <select id="ProjectType" class="custom-select">
                        <option value="">Select a service</option>
                        <option value="web">Web Development</option>
                        <option value="mobile">Mobile Apps</option>
                        <option value="uiux">UI/UX Design</option>
                        <option value="seo">SEO & Marketing</option>
                      </select>
                    </div>
                  </div>
                  <div class="col-lg-12">
                    <div class="mainInput">
                      <label for="ProjectDetails">Your Message</label>
                      <textarea
                        cols="30"
                        rows="4"
                        id="ProjectDetails"
                        placeholder="Tell us about your project or inquiry..."
                        required
                      ></textarea>
                    </div>
                  </div>
                </div>
                <button type="submit" class="mainBtn w-100">
                  Send Inquiry
                </button>
              </form>
            </div>
          </div>
        </div>

        <!-- Google Map Section -->
        <div class="map-section mt-5">
          <div
            class="glass-card p-0 overflow-hidden"
            style="border-radius: 20px"
          >
            <iframe
              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d184552.571600865!2d-79.51814051!3d43.7181557!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x89d4cb90d7c69ba5%3A0x88db121d80117b84!2sToronto%2C%20ON%2C%20Canada!5e0!3m2!1sen!2sus!4v1710423000000!5m2!1sen!2sus"
              width="100%"
              height="450"
              style="border: 0"
              allowfullscreen=""
              loading="lazy"
              referrerpolicy="no-referrer-when-downgrade"
            >
            </iframe>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      imgUrl: require("../../../imgs/pages/contact/contact_hero_bg.webp"),
    };
  },
  mounted() {
    const content = document.querySelector(".baseHero");
    const imgload = this.$imagesLoaded(content);
    imgload.on("done", () => {
      this.$store.dispatch("doneLoading", true);
    });
  },
};
</script>

<style lang="scss" scoped>
.contactPage {
  background: var(--bg-dark);
  min-height: 100vh;

  .content {
    padding-bottom: 120px;

    .head {
      margin-bottom: 40px;

      .mainTitle {
        font-family: var(--font-heading);
        font-size: 56px;
        line-height: 1.1;
        font-weight: 800;
        margin-top: 15px;
        color: var(--text-main);

        @media (max-width: 991px) {
          font-size: 38px;
        }
      }
    }

    .info {
      .mainP {
        font-size: 18px;
        color: var(--text-muted);
        line-height: 1.8;
        margin-bottom: 35px;
      }

      .contact-details {
        display: flex;
        flex-direction: column;
        gap: 30px;
        padding: 0;
        margin-bottom: 40px;

        li {
          display: flex;
          align-items: center;
          gap: 20px;

          .icon-box {
            width: 55px;
            height: 55px;
            background: rgba(255, 196, 46, 0.1);
            border: 1px solid rgba(255, 196, 46, 0.2);
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 20px;
            color: var(--sec-color);
            transition: var(--transition);
          }

          .text {
            span {
              display: block;
              font-size: 14px;
              color: var(--sec-color);
              text-transform: uppercase;
              letter-spacing: 1.5px;
              font-weight: 700;
              margin-bottom: 4px;
            }
            p {
              margin: 0;
              font-size: 18px;
              color: var(--text-main);
              font-weight: 600;
            }
          }

          &:hover .icon-box {
            background: var(--sec-color);
            color: black;
            transform: translateY(-5px);
          }
        }
      }

      .whatsapp-btn {
        display: inline-flex;
        align-items: center;
        gap: 12px;
        background: #25d366;
        color: white;
        padding: 15px 30px;
        border-radius: 12px;
        text-decoration: none;
        font-weight: 700;
        transition: var(--transition);
        box-shadow: 0 10px 20px rgba(37, 211, 102, 0.2);

        svg {
          font-size: 24px;
        }

        &:hover {
          transform: translateY(-3px);
          box-shadow: 0 15px 30px rgba(37, 211, 102, 0.3);
          background: #20bd5a;
        }
      }
    }

    .contact-form-wrapper {
      background: var(--glass-card);
      border: 1px solid var(--glass-border);
      border-radius: 25px;
      box-shadow: var(--shadow-premium);

      .mainInput {
        margin-bottom: 25px;

        label {
          display: block;
          margin-bottom: 10px;
          color: var(--text-main);
          font-weight: 600;
          font-size: 14px;
          text-transform: uppercase;
          letter-spacing: 1px;
        }

        input,
        textarea,
        .custom-select {
          width: 100%;
          background: rgba(255, 255, 255, 0.05);
          border: 1px solid var(--glass-border);
          border-radius: 12px;
          padding: 15px 20px;
          color: var(--text-main);
          font-family: var(--font-body);
          transition: var(--transition);
          appearance: none;

          &:focus {
            outline: none;
            border-color: var(--sec-color);
            background: rgba(255, 255, 255, 0.08);
            box-shadow: 0 0 15px rgba(255, 196, 46, 0.1);
          }

          &::placeholder {
            color: rgba(255, 255, 255, 0.2);
          }
        }

        .custom-select {
          cursor: pointer;
          background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='24' height='24' viewBox='0 0 24 24' fill='none' stroke='rgba(255,255,255,0.5)' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'%3E%3Cpolyline points='6 9 12 15 18 9'%3E%3C/polyline%3E%3C/svg%3E");
          background-repeat: no-repeat;
          background-position: right 15px center;
          background-size: 18px;

          option {
            background: #1a1a1a;
            color: white;
          }
        }
      }
    }
  }
}
</style>
