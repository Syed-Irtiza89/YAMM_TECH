<template>
  <footer class="premium-footer">
    <div class="container">
      <div class="footer-main">
        <div class="row g-5">
          <!-- Column 1: Logo & About -->
          <div class="col-lg-4 col-md-12">
            <div class="footer-brand">
              <router-link to="/" class="logo">
                <img
                  src="../../../imgs/homeAssets/yamm_tech_logo.png"
                  alt="YammTech Logo"
                />
                <span class="logo-text">YAMM <span>TECH</span></span>
              </router-link>
              <p class="mt-4">
                Empowering businesses with enterprise-grade software solutions.
                We specialize in high-performance web and mobile products that
                drive digital innovation and measurable growth.
              </p>
              <div class="social-wrapper mt-4">
                <a href="#" class="social-link" aria-label="LinkedIn">
                  <font-awesome-icon icon="fa-brands fa-linkedin-in" />
                </a>
                <a href="#" class="social-link" aria-label="Github">
                  <font-awesome-icon icon="fa-brands fa-github" />
                </a>
                <a href="#" class="social-link" aria-label="X-Twitter">
                  <font-awesome-icon icon="fa-brands fa-x-twitter" />
                </a>
                <a href="#" class="social-link" aria-label="Instagram">
                  <font-awesome-icon icon="fa-brands fa-instagram" />
                </a>
              </div>
            </div>
          </div>

          <!-- Column 2: Quick Links -->
          <div class="col-lg-2 col-md-4 col-6">
            <h5 class="footer-head">Company</h5>
            <ul class="footer-links">
              <li><router-link to="/">Home</router-link></li>
              <li><router-link to="/about">About Us</router-link></li>
              <li><router-link to="/portfolio">Portfolio</router-link></li>
              <li><router-link to="/services">Services</router-link></li>
              <li><router-link to="/contact">Contact</router-link></li>
            </ul>
          </div>

          <!-- Column 3: Services -->
          <div class="col-lg-3 col-md-4 col-6">
            <h5 class="footer-head">Services</h5>
            <ul class="footer-links">
              <li><router-link to="/services">Web Development</router-link></li>
              <li><router-link to="/services">Mobile Apps</router-link></li>
              <li><router-link to="/services">UI/UX Design</router-link></li>
              <li><router-link to="/services">SEO Marketing</router-link></li>
              <li><router-link to="/services">Cloud Solutions</router-link></li>
            </ul>
          </div>

          <!-- Column 4: Newsletter -->
          <div class="col-lg-3 col-md-4">
            <h5 class="footer-head">Stay Updated</h5>
            <p class="small text-muted mb-4">
              Subscribe for the latest tech insights.
            </p>
            <div class="newsletter-form">
              <input
                type="email"
                placeholder="Email address"
                class="newsletter-input"
              />
              <button class="newsletter-btn">
                <font-awesome-icon icon="fa-solid fa-paper-plane" />
              </button>
            </div>
            <div class="contact-compact mt-4">
              <div class="contact-item">
                <font-awesome-icon icon="fa-solid fa-phone" />
                <span>+1 (437) 559-1485</span>
              </div>
              <div class="contact-item">
                <font-awesome-icon icon="fa-solid fa-envelope" />
                <span>info@yammtech.com</span>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Footer Bottom -->
      <div class="footer-bottom">
        <div class="copyright">
          &copy; 2025 <span class="text-gold">YammTech</span>. All Rights
          Reserved.
        </div>
        <div class="legal-links">
          <router-link to="/terms">Terms</router-link>
          <router-link to="/privacy">Privacy</router-link>
        </div>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
.premium-footer {
  background: linear-gradient(180deg, #0a0a0a 0%, #050505 100%);
  padding: 100px 20px 0;
  border-top: 1px solid rgba(255, 255, 255, 0.05);
  position: relative;
  overflow: hidden;

  &::before {
    content: "";
    position: absolute;
    top: 0;
    left: 50%;
    transform: translateX(-50%);
    width: 80%;
    height: 1px;
    background: linear-gradient(
      90deg,
      transparent,
      var(--sec-color),
      transparent
    );
    opacity: 0.3;
  }

  .footer-main {
    padding-bottom: 80px;
  }

  .footer-brand {
    .logo {
      display: flex;
      align-items: center;
      gap: 12px;
      text-decoration: none;

      img {
        height: 40px;
        filter: drop-shadow(0 0 10px rgba(255, 196, 46, 0.2));
      }

      .logo-text {
        font-family: var(--font-heading);
        font-size: 24px;
        font-weight: 800;
        color: white;
        letter-spacing: 1px;

        span {
          color: var(--sec-color);
        }
      }
    }

    p {
      color: rgba(255, 255, 255, 0.6);
      line-height: 1.8;
      font-size: 15px;
      max-width: 320px;
    }
  }

  .social-wrapper {
    display: flex;
    gap: 12px;

    .social-link {
      width: 42px;
      height: 42px;
      border-radius: 12px;
      background: rgba(255, 255, 255, 0.05);
      border: 1px solid rgba(255, 255, 255, 0.1);
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      text-decoration: none;
      transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);

      &:hover {
        background: var(--sec-color);
        color: black;
        transform: translateY(-5px);
        border-color: var(--sec-color);
        box-shadow: 0 10px 20px rgba(255, 196, 46, 0.2);
      }
    }
  }

  .footer-head {
    color: white;
    font-family: var(--font-heading);
    font-weight: 700;
    font-size: 18px;
    margin-bottom: 30px;
    position: relative;
    padding-bottom: 12px;

    &::after {
      content: "";
      position: absolute;
      bottom: 0;
      left: 0;
      width: 30px;
      height: 2px;
      background: var(--sec-color);
    }
  }

  .footer-links {
    list-style: none;
    padding: 0;
    margin: 0;

    li {
      margin-bottom: 12px;

      a {
        color: rgba(255, 255, 255, 0.5);
        text-decoration: none;
        font-size: 15px;
        transition: all 0.3s ease;

        &:hover {
          color: var(--sec-color);
          padding-left: 5px;
        }
      }
    }
  }

  .newsletter-form {
    display: flex;
    background: rgba(255, 255, 255, 0.05);
    border: 1px solid rgba(255, 255, 255, 0.1);
    border-radius: 12px;
    padding: 6px;
    margin-bottom: 20px;
    transition: var(--transition);

    &:focus-within {
      border-color: var(--sec-color);
      background: rgba(255, 255, 255, 0.08);
    }

    .newsletter-input {
      background: transparent;
      border: none;
      padding: 10px 15px;
      color: white;
      width: 100%;
      font-size: 14px;

      &:focus {
        outline: none;
      }
    }

    .newsletter-btn {
      background: var(--sec-color);
      border: none;
      border-radius: 8px;
      width: 42px;
      height: 42px;
      display: flex;
      align-items: center;
      justify-content: center;
      color: black;
      transition: var(--transition);

      &:hover {
        transform: scale(1.05);
        background: white;
      }
    }
  }

  .contact-compact {
    .contact-item {
      display: flex;
      align-items: center;
      gap: 12px;
      color: rgba(255, 255, 255, 0.6);
      font-size: 14px;
      margin-bottom: 12px;

      svg {
        color: var(--sec-color);
        font-size: 14px;
      }
    }
  }

  .footer-bottom {
    padding: 30px 0;
    border-top: 1px solid rgba(255, 255, 255, 0.05);
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 14px;

    @media (max-width: 767px) {
      flex-direction: column;
      gap: 15px;
      text-align: center;
    }

    .copyright {
      color: rgba(255, 255, 255, 0.4);

      .text-gold {
        color: var(--sec-color);
        font-weight: 600;
      }
    }

    .legal-links {
      display: flex;
      gap: 25px;

      a {
        color: rgba(255, 255, 255, 0.4);
        text-decoration: none;
        transition: var(--transition);

        &:hover {
          color: white;
        }
      }
    }
  }
}
</style>
