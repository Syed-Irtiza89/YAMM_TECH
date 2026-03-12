<template>
  <footer>
    <div class="container">
      <div class="footer-main">
        <div class="row">
          <!-- Column 1: Logo & About -->
          <div class="col-lg-3 col-md-6 col-12">
            <div class="logo">
              <img
                src="../../../imgs/homeAssets/footer_logo.svg"
                alt="YammTech Logo"
              />
            </div>
            <p>
              YammTech delivers enterprise-grade software solutions to
              businesses worldwide. From concept to deployment, we build digital
              products that drive growth and innovation.
            </p>
            <div class="socials">
              <div class="social">
                <font-awesome-icon icon="fa-brands fa-linkedin-in" />
              </div>
              <div class="social">
                <font-awesome-icon icon="fa-brands fa-x-twitter" />
              </div>
              <div class="social">
                <font-awesome-icon icon="fa-brands fa-github" />
              </div>
            </div>
          </div>

          <!-- Column 2: Services -->
          <div class="col-lg-3 col-md-6 col-12">
            <span class="head">Our Services</span>
            <ul class="links">
              <li>Website Development</li>
              <li>Mobile Applications</li>
              <li>SEO & Digital Marketing</li>
              <li>3D Rendering</li>
              <li>Technology Consulting</li>
            </ul>
          </div>

          <!-- Column 3: Contact Info -->
          <div class="col-lg-3 col-md-6 col-12">
            <span class="head">Contact Us</span>
            <ul class="contact-info">
              <li>
                <font-awesome-icon icon="fa-solid fa-location-dot" />
                <span>123 Business Avenue, Tech Park, City - 400001</span>
              </li>
              <li>
                <font-awesome-icon icon="fa-solid fa-phone" />
                <span>+91 98765 43210</span>
              </li>
              <li>
                <font-awesome-icon icon="fa-solid fa-envelope" />
                <span>hello@yammtech.com</span>
              </li>
            </ul>
          </div>

          <!-- Column 4: Subscribe -->
          <div class="col-lg-3 col-md-6 col-12">
            <span class="head">Stay Updated</span>
            <div class="inputgroup mainSubmit">
              <input
                id="footeremail"
                type="email"
                placeholder="Enter your email"
              />
              <button class="mainBtn" id="footersend">Subscribe</button>
            </div>
            <p class="subscribe-text">
              Get the latest insights on technology trends, software
              development, and digital transformation delivered to your inbox.
            </p>
          </div>
        </div>
      </div>

      <!-- Footer Bottom -->
      <div class="footer-bottom">
        <div class="copyright">© 2024 YammTech. All rights reserved.</div>
        <div class="terms-privacy">
          <span>Terms of Use</span>
          <span>Privacy Policy</span>
        </div>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
:root {
  --yammtech-blue: #1f51fe;
  --yammtech-yellow: #ffc42e;
}

@media (max-width: 991px) {
  footer {
    margin-top: 60px !important;
  }
}

footer {
  margin-top: 95px;
  color: #fefefeb3;
  background: linear-gradient(267.18deg, #161616 0%, #080808 100%);
  padding: 60px 0 0;

  @media (max-width: 991px) {
    .footer-main {
      padding-bottom: 15px !important;
    }
  }

  .footer-main {
    padding-bottom: 35px;

    .row {
      & > div {
        margin-bottom: 40px;
      }

      // Logo & About Section
      .logo {
        margin-bottom: 20px;

        img {
          height: 40px;
          width: auto;
        }
      }

      .logo ~ p {
        margin: 0 0 20px;
        font-size: 15px;
        line-height: 1.7;
        color: #fefefeb3;
      }

      // Social Icons
      .socials {
        color: white;
        margin-top: 15px;
        display: flex;
        align-items: center;
        justify-content: start;
        gap: 12px;

        .social {
          display: flex;
          align-items: center;
          justify-content: center;
          width: 40px;
          height: 40px;
          border-radius: 50%;
          border: 2px solid rgba(255, 255, 255, 0.2);
          cursor: pointer;
          transition: all 0.3s ease;
          color: white;

          @media (min-width: 992px) {
            &:hover {
              border-color: var(--yammtech-blue);
              background-color: var(--yammtech-blue);
              transform: translateY(-3px);
            }
          }

          svg {
            font-size: 18px;
          }
        }
      }

      // Section Headers
      .head {
        display: block;
        margin-bottom: 25px;
        color: white;
        font-size: 18px;
        font-weight: 600;
        position: relative;
        padding-bottom: 10px;

        &::after {
          content: "";
          position: absolute;
          bottom: 0;
          left: 0;
          width: 40px;
          height: 3px;
          background: var(--yammtech-blue);
        }
      }

      // Services List
      ul.links {
        list-style: none;
        padding: 0;
        margin: 0;

        li {
          color: #fefefeb3;
          transition: all 0.3s ease;
          cursor: pointer;
          margin-bottom: 12px;
          font-size: 15px;

          @media (min-width: 992px) {
            &:hover {
              color: var(--yammtech-blue);
              transform: translateX(5px);
            }
          }
        }
      }

      // Contact Info with Icons
      ul.contact-info {
        list-style: none;
        padding: 0;
        margin: 0;

        li {
          display: flex;
          align-items: flex-start;
          gap: 12px;
          margin-bottom: 15px;
          font-size: 15px;
          line-height: 1.6;

          svg {
            color: var(--yammtech-blue);
            font-size: 16px;
            margin-top: 3px;
            min-width: 16px;
          }

          span {
            color: #fefefeb3;
          }
        }
      }

      // Subscribe Section
      .inputgroup {
        display: flex;
        gap: 10px;
        margin-bottom: 15px;

        input {
          flex: 1;
          background: rgba(255, 255, 255, 0.05);
          border: 1px solid rgba(255, 255, 255, 0.1);
          border-radius: 8px;
          padding: 12px 15px;
          color: white;
          font-size: 14px;
          transition: all 0.3s ease;

          &:focus {
            outline: none;
            border-color: var(--yammtech-blue);
            background: rgba(31, 81, 254, 0.1);
          }

          &::placeholder {
            color: rgba(255, 255, 255, 0.4);
          }
        }

        .mainBtn {
          background: var(--yammtech-blue);
          border: none;
          border-radius: 8px;
          padding: 0 20px;
          color: white;
          font-size: 14px;
          font-weight: 500;
          cursor: pointer;
          transition: all 0.3s ease;
          white-space: nowrap;

          @media (min-width: 992px) {
            &:hover {
              background: #0a3bff;
              transform: translateY(-2px);
              box-shadow: 0 5px 15px rgba(31, 81, 254, 0.3);
            }
          }
        }
      }

      .subscribe-text {
        font-size: 14px;
        line-height: 1.7;
        color: #fefefeb3;
        margin: 15px 0 0;
      }
    }
  }

  // Footer Bottom
  .footer-bottom {
    padding: 20px 0;
    display: flex;
    align-items: center;
    justify-content: space-between;
    border-top: 1px solid rgba(255, 255, 255, 0.1);
    font-size: 14px;

    @media (max-width: 767px) {
      flex-direction: column;
      gap: 15px;
      text-align: center;
    }

    .copyright {
      color: #fefefeb3;
    }

    .terms-privacy {
      display: flex;
      gap: 20px;

      span {
        color: #fefefeb3;
        cursor: pointer;
        transition: color 0.3s ease;
        position: relative;

        &:first-child {
          &::after {
            content: "";
            position: absolute;
            right: -10px;
            top: 50%;
            transform: translateY(-50%);
            width: 1px;
            height: 12px;
            background-color: rgba(255, 255, 255, 0.2);
          }
        }

        @media (min-width: 992px) {
          &:hover {
            color: var(--yammtech-blue);
          }
        }
      }
    }
  }
}
</style>
