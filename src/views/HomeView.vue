<template>
  <div class="homePage">
    <!-- HERO SECTION - Keep -->
    <div class="hero">
      <div class="container">
        <div class="content">
          <div class="shape"></div>
          <div class="shape"></div>
          <div class="shape"></div>
          <h1 class="head">
            Elevate Your Business with <br />
            <span class="text-gradient">Smart Digital Solutions</span>
          </h1>
          <div class="getaQuote">
            <p>
              At YammTech, we’re a full-service digital agency specializing in
              beautiful UI/UX design, fast website development, powerful mobile
              apps, result-driven SEO, digital marketing, fintech software, AI
              video creation, and stunning interior 3D renderings — all designed
              to help your business grow.
            </p>
            <div class="hero-btns d-flex flex-wrap gap-3">
              <router-link to="/contact">
                <div class="mainBtn">Book a Free Consultation</div>
              </router-link>
              <router-link to="/services">
                <div class="secondBtn basic">Explore Services</div>
              </router-link>
            </div>
          </div>

          <!-- Trust Indicators -->
          <div class="hero-trust-indicators d-flex flex-wrap gap-4 mt-5">
            <div class="trust-item">
              <span class="num">10+</span>
              <span class="label">Years of <br />Expertise</span>
            </div>
            <div class="trust-item">
              <span class="num">500+</span>
              <span class="label">Projects <br />Delivered</span>
            </div>
            <div class="trust-item">
              <span class="num">99%</span>
              <span class="label">Client <br />Satisfaction</span>
            </div>
          </div>

          <div class="scroll-indicator-wrap">
            <div class="scroll-mouse">
              <div class="scroll-wheel"></div>
            </div>
            <span>Scroll to Explore</span>
          </div>
        </div>
      </div>
      <div class="follow-us">
        <span>follow us</span>
        <span>linkedin</span>
        <span>github</span>
      </div>
    </div>

    <!-- NUMBERS SECTION - Keep (rename later) -->
    <div class="ourFunFact">
      <div class="container">
        <div class="statusBorder">
          <img
            src="../../imgs/homeAssets/funfact_shape_bg.svg"
            alt="ourFunfact Svg"
          />
          <div class="status">
            <div class="info">
              <h1>Grow Smarter with a Partner You Can Trust</h1>
              <p>
                YammTech is more than just another software development company.
                We partner with startups, growing businesses, and established
                brands to turn ideas into high-performing digital products that
                actually deliver results.
              </p>
              <p>
                Our team blends creative UI/UX design, clean code, strategic SEO
                & marketing, and innovative tech (like AI tools and fintech
                systems) so you get solutions built for real users — and real
                business growth.
              </p>
              <p>
                We care about performance, clean user experiences, and long-term
                success — not just shipping a project and moving on.
              </p>
            </div>
            <div class="nums row gy-3">
              <div class="num col-md-6 col-12">
                <div class="odo">
                  <span data-numm="99" class="odometer">5</span>
                  <span class="kword">+</span>
                </div>
                <div class="title">
                  <span>Global Happy Clients</span>
                </div>
              </div>
              <div class="num col-md-6 col-12">
                <div class="odo">
                  <span data-numm="300" class="odometer">50</span>
                  <span class="kword">+</span>
                </div>
                <div class="title">
                  <span>Project Completed</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- WHY CHOOSE US SECTION - New -->
    <div class="why-choose-us mainPadding">
      <div class="container">
        <div class="text-center mb-5">
          <span class="homeheadsec">Why Choose YammTech</span>
          <h2 class="mainTitle">Building Digital Future with Excellence</h2>
        </div>
        <div class="row g-4">
          <div class="col-lg-4 col-md-6 choose-item">
            <div class="glass-card feature-block p-4 h-100">
              <div class="icon-wrap mb-3">
                <font-awesome-icon icon="fa-solid fa-users" class="icon-gold" />
              </div>
              <h3>Professional Team</h3>
              <p>
                Our experts bring years of industry experience to deliver
                world-class solutions for your business.
              </p>
            </div>
          </div>
          <div class="col-lg-4 col-md-6 choose-item">
            <div class="glass-card feature-block p-4 h-100">
              <div class="icon-wrap mb-3">
                <font-awesome-icon icon="fa-solid fa-award" class="icon-gold" />
              </div>
              <h3>High Quality Work</h3>
              <p>
                We don't just build; we craft. Our focus is on clean code,
                stunning design, and pixel-perfect results.
              </p>
            </div>
          </div>
          <div class="col-lg-4 col-md-6 choose-item">
            <div class="glass-card feature-block p-4 h-100">
              <div class="icon-wrap mb-3">
                <font-awesome-icon icon="fa-solid fa-tags" class="icon-gold" />
              </div>
              <h3>Affordable Pricing</h3>
              <p>
                Get premium digital services at competitive rates designed to
                fit your budget without compromising quality.
              </p>
            </div>
          </div>
          <div class="col-lg-4 col-md-6 choose-item">
            <div class="glass-card feature-block p-4 h-100">
              <div class="icon-wrap mb-3">
                <font-awesome-icon
                  icon="fa-solid fa-rocket"
                  class="icon-gold"
                />
              </div>
              <h3>Fast Project Delivery</h3>
              <p>
                We value your time. Our streamlined process ensures your project
                is completed and launched on schedule.
              </p>
            </div>
          </div>
          <div class="col-lg-4 col-md-6 choose-item">
            <div class="glass-card feature-block p-4 h-100">
              <div class="icon-wrap mb-3">
                <font-awesome-icon
                  icon="fa-solid fa-face-smile"
                  class="icon-gold"
                />
              </div>
              <h3>Customer Satisfaction</h3>
              <p>
                Your success is our priority. We work closely with you to ensure
                the final product exceeds your expectations.
              </p>
            </div>
          </div>
          <div class="col-lg-4 col-md-6 choose-item">
            <div class="glass-card feature-block p-4 h-100">
              <div class="icon-wrap mb-3">
                <font-awesome-icon
                  icon="fa-solid fa-shield-halved"
                  class="icon-gold"
                />
              </div>
              <h3>Trust & Scalability</h3>
              <p>
                Our code is built to last. We prioritize security and
                scalability so your platform grows as your business does.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- SERVICES SECTION - Keep -->
    <div class="services" id="#services">
      <div class="container">
        <div class="content">
          <div class="row">
            <div class="col-xl-4 col-12 info">
              <span class="homeheadsec">What Can We Do</span>
              <p class="mainTitle">Services we can help you with</p>
              <router-link aria-label="services" to="/services">
                <div class="servicesbtn goToBtn">
                  <div class="hoveranim">See All Services</div>
                  <font-awesome-icon icon="fa-solid fa-arrow-right-long" />
                </div>
              </router-link>
            </div>
            <div class="col-xl-8 col-12 row services-grid">
              <!-- UI/UX Design -->
              <div class="col-lg-4 col-sm-6 mb-4">
                <div class="glass-card service-box p-4">
                  <div class="icon-box mb-3">
                    <font-awesome-icon
                      icon="fa-solid fa-pen-nib"
                      class="icon-gold"
                    />
                  </div>
                  <h3 class="title">UI/UX Design</h3>
                  <p class="desc">
                    Creating beautiful, intuitive interfaces that users love to
                    engage with.
                  </p>
                  <router-link to="/services" class="learn-more">
                    <span>Learn More</span>
                    <font-awesome-icon icon="fa-solid fa-arrow-right" />
                  </router-link>
                </div>
              </div>
              <!-- Web Development -->
              <div class="col-lg-4 col-sm-6 mb-4">
                <div class="glass-card service-box p-4">
                  <div class="icon-box mb-3">
                    <font-awesome-icon
                      icon="fa-solid fa-code"
                      class="icon-gold"
                    />
                  </div>
                  <h3 class="title">Web Development</h3>
                  <p class="desc">
                    Building fast, responsive, and high-performing websites
                    tailored to your needs.
                  </p>
                  <router-link to="/services" class="learn-more">
                    <span>Learn More</span>
                    <font-awesome-icon icon="fa-solid fa-arrow-right" />
                  </router-link>
                </div>
              </div>
              <!-- Mobile Apps -->
              <div class="col-lg-4 col-sm-6 mb-4">
                <div class="glass-card service-box p-4">
                  <div class="icon-box mb-3">
                    <font-awesome-icon
                      icon="fa-solid fa-mobile-screen-button"
                      class="icon-gold"
                    />
                  </div>
                  <h3 class="title">Mobile Apps</h3>
                  <p class="desc">
                    Scalable mobile solutions for iOS and Android that drive
                    business growth.
                  </p>
                  <router-link to="/services" class="learn-more">
                    <span>Learn More</span>
                    <font-awesome-icon icon="fa-solid fa-arrow-right" />
                  </router-link>
                </div>
              </div>
              <!-- SEO & SEM -->
              <div class="col-lg-4 col-sm-6 mb-4">
                <div class="glass-card service-box p-4">
                  <div class="icon-box mb-3">
                    <font-awesome-icon
                      icon="fa-solid fa-magnifying-glass-chart"
                      class="icon-gold"
                    />
                  </div>
                  <h3 class="title">SEO & SEM</h3>
                  <p class="desc">
                    Boost your visibility and drive organic traffic with our
                    data-driven strategies.
                  </p>
                  <router-link to="/services" class="learn-more">
                    <span>Learn More</span>
                    <font-awesome-icon icon="fa-solid fa-arrow-right" />
                  </router-link>
                </div>
              </div>
              <!-- Digital Marketing -->
              <div class="col-lg-4 col-sm-6 mb-4">
                <div class="glass-card service-box p-4">
                  <div class="icon-box mb-3">
                    <font-awesome-icon
                      icon="fa-solid fa-bullhorn"
                      class="icon-gold"
                    />
                  </div>
                  <h3 class="title">Digital Marketing</h3>
                  <p class="desc">
                    Scale your brand with targeted campaigns and comprehensive
                    marketing solutions.
                  </p>
                  <router-link to="/services" class="learn-more">
                    <span>Learn More</span>
                    <font-awesome-icon icon="fa-solid fa-arrow-right" />
                  </router-link>
                </div>
              </div>
              <!-- Fintech Solutions -->
              <div class="col-lg-4 col-sm-6 mb-4">
                <div class="glass-card service-box p-4">
                  <div class="icon-box mb-3">
                    <font-awesome-icon
                      icon="fa-solid fa-coins"
                      class="icon-gold"
                    />
                  </div>
                  <h3 class="title">Fintech Solutions</h3>
                  <p class="desc">
                    Secure, innovative software solutions for the modern
                    financial landscape.
                  </p>
                  <router-link to="/services" class="learn-more">
                    <span>Learn More</span>
                    <font-awesome-icon icon="fa-solid fa-arrow-right" />
                  </router-link>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- PORTFOLIO SECTION - Keep -->
    <div class="portfolio">
      <div class="content">
        <div
          class="head text-center mb-5 d-flex flex-column align-items-center justify-content-center"
        >
          <div class="head-text">
            <div class="homeheadsec text-center">Latest Projects</div>
            <h1 class="text-center">Portfolio to explore</h1>
          </div>
          <router-link to="/portfolio" class="servicesbtn goToBtn mt-3">
            <div class="hoveranim">View All Projects</div>
            <font-awesome-icon icon="fa-solid fa-arrow-right-long" />
          </router-link>
        </div>
        <transition name="dataFadein">
          <div
            v-show="PortfolioDataLoaded"
            class="swiper-container"
            ref="portSwiper"
          >
            <div class="swiper-wrapper">
              <div
                class="swiper-slide"
                v-for="(post, index) in getProjectsData"
                :key="index"
              >
                <div class="slide">
                  <div class="img">
                    <router-link
                      aria-label="portfolio"
                      :to="'/portfolioDetails/' + post.id"
                    >
                      <img
                        :src="getProjectImg(post, index)"
                        :alt="post.title"
                      />
                      <div class="overlay">
                        <div class="project-info">
                          <span class="category">{{
                            post.category || "Digital Solution"
                          }}</span>
                          <h3 class="title">{{ post.title }}</h3>
                          <div class="view-btn">
                            <span>See Details</span>
                            <font-awesome-icon icon="fa-solid fa-arrow-right" />
                          </div>
                        </div>
                      </div>
                    </router-link>
                  </div>
                </div>
              </div>
            </div>
            <div class="swiper-pagination"></div>
          </div>
        </transition>
        <loading-spinner v-show="!PortfolioDataLoaded"></loading-spinner>
      </div>
    </div>

    <!-- TEAM SECTION - Keep -->
    <div class="ourTeam">
      <div class="container">
        <div class="content">
          <div class="controls text-center justify-content-center mb-5">
            <div class="head">
              <div class="homeheadsec slidOurTeam mx-auto">Our Team</div>
              <h2 class="mainTitle text-center">Awesome team members</h2>
            </div>
          </div>
          <transition name="dataFadein">
            <div class="swiper-container team-text-slider" ref="teamSwiper">
              <div class="swiper-wrapper">
                <div
                  class="swiper-slide"
                  v-for="(member, index) in newTeamMembers"
                  :key="index"
                >
                  <div class="memberCard text-center">
                    <div class="member-info-card">
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
              </div>
              <div class="swiper-pagination"></div>
            </div>
          </transition>
          <loading-spinner v-show="!teamDataLoaded"></loading-spinner>
        </div>
      </div>
    </div>

    <div class="comments">
      <div class="container">
        <div class="text-center mb-5">
          <span class="homeheadsec text-center">Testimonials</span>
          <h2 class="mainTitle text-center">What Our Clients Say</h2>
        </div>

        <div
          class="swiper-container testimonials-swiper"
          ref="testimonialsSwiper"
        >
          <div class="swiper-wrapper">
            <!-- Testimonial 1 -->
            <div class="swiper-slide">
              <div class="testimonial-card">
                <div class="card-header">
                  <div class="client-img">
                    <img src="../../imgs/homeAssets/testimonial_1.webp" alt="Jasmine Rivera" />
                  </div>
                  <div class="client-details">
                    <h4 class="name">Jasmine Rivera</h4>
                    <span class="role">Marketing Analyst</span>
                  </div>
                </div>
                <div class="stars">
                  <font-awesome-icon icon="fa-solid fa-star" />
                  <font-awesome-icon icon="fa-solid fa-star" />
                  <font-awesome-icon icon="fa-solid fa-star" />
                  <font-awesome-icon icon="fa-solid fa-star" />
                  <font-awesome-icon icon="fa-solid fa-star" />
                </div>
                <p class="review">
                  "I wish I would have thought of it first. Creative agency is
                  the most tech valuable business resource we have ever
                  purchased. Your stuff is the bomb! Veritatis et quasi
                  architecto beatae vitae dicta sunt to the explicabo."
                </p>
                <font-awesome-icon icon="fa-solid fa-quote-right" class="quote-bg" />
              </div>
            </div>

            <!-- Testimonial 2 -->
            <div class="swiper-slide">
              <div class="testimonial-card">
                <div class="card-header">
                  <div class="client-img">
                    <img src="../../imgs/homeAssets/testimonial_2.webp" alt="Ethan Carter" />
                  </div>
                  <div class="client-details">
                    <h4 class="name">Ethan Carter</h4>
                    <span class="role">Software Engineer</span>
                  </div>
                </div>
                <div class="stars">
                  <font-awesome-icon icon="fa-solid fa-star" />
                  <font-awesome-icon icon="fa-solid fa-star" />
                  <font-awesome-icon icon="fa-solid fa-star" />
                  <font-awesome-icon icon="fa-solid fa-star" />
                  <font-awesome-icon icon="fa-solid fa-star" class="deactive" />
                </div>
                <p class="review">
                  "Investing in creative agency has proven to be the most
                  invaluable tech resource we've ever acquired. Your work is
                  absolutely fantastic! It's like the words of praise that come
                  straight from the creator himself."
                </p>
                <font-awesome-icon icon="fa-solid fa-quote-right" class="quote-bg" />
              </div>
            </div>

            <!-- Testimonial 3 -->
            <div class="swiper-slide">
              <div class="testimonial-card">
                <div class="card-header">
                  <div class="client-img">
                    <img src="../../imgs/homeAssets/testimonial_3.webp" alt="Olivia Bennett" />
                  </div>
                  <div class="client-details">
                    <h4 class="name">Olivia Bennett</h4>
                    <span class="role">Financial Planner</span>
                  </div>
                </div>
                <div class="stars">
                  <font-awesome-icon icon="fa-solid fa-star" />
                  <font-awesome-icon icon="fa-solid fa-star" />
                  <font-awesome-icon icon="fa-solid fa-star" />
                  <font-awesome-icon icon="fa-solid fa-star" />
                  <font-awesome-icon icon="fa-solid fa-star" />
                </div>
                <p class="review">
                  "Our investment in creative agency has turned out to be the
                  ultimate tech asset we've ever secured. Your work is simply
                  mind-blowing! Every word you craft unveils the secrets of
                  excellence."
                </p>
                <font-awesome-icon icon="fa-solid fa-quote-right" class="quote-bg" />
              </div>
            </div>
          </div>
          <div class="swiper-pagination"></div>
        </div>
      </div>
    </div>

    <div class="partners py-5">
      <div class="container">
        <div class="partners-info text-center mb-5">
          <h2 class="text-white mb-3">Our Trusted Partners</h2>
          <p class="text-white-50 mx-auto" style="max-width: 600px; color: rgba(255, 255, 255, 0.9) !important;">
            We collaborate with industry leaders to deliver the best solutions
            for our clients.
          </p>
        </div>
        <div class="partners-slider-wrap">
          <div class="swiper partners-slider" ref="partnersSwiper">
            <div class="swiper-wrapper">
              <div class="swiper-slide brand-logo">
                <img
                  src="../../imgs/homeAssets/partner_1.svg"
                  alt="partner_1"
                />
              </div>
              <div class="swiper-slide brand-logo">
                <img
                  src="../../imgs/homeAssets/partner_2.svg"
                  alt="partner_2"
                />
              </div>
              <div class="swiper-slide brand-logo">
                <img
                  src="../../imgs/homeAssets/partner_3.svg"
                  alt="partner_3"
                />
              </div>
              <div class="swiper-slide brand-logo">
                <img
                  src="../../imgs/homeAssets/partner_4.svg"
                  alt="partner_4"
                />
              </div>
              <div class="swiper-slide brand-logo">
                <img
                  src="../../imgs/homeAssets/partner_5.svg"
                  alt="partner_5"
                />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- CTA SECTION -->
    <div class="cta-section mainPadding">
      <div class="container">
        <div class="cta-content p-5 text-center position-relative">
          <div class="shape"></div>
          <div class="shape"></div>
          <h2 class="cta-title">Ready to Transform Your Digital Presence?</h2>
          <p class="cta-desc">
            Join hundreds of successful businesses that have scaled with our
            premium digital solutions.
          </p>
          <router-link
            to="/contact"
            class="mainBtn d-inline-flex align-items-center gap-2 mt-2"
          >
            Start Your Project Now
            <font-awesome-icon icon="fa-solid fa-arrow-right" />
          </router-link>
        </div>
      </div>
    </div>

    <!-- CONTACT PREVIEW SECTION -->
    <div class="contact-preview">
      <div class="container">
        <div class="row align-items-center g-5">
          <div class="col-lg-7">
            <h2 class="section-title">
              Let's build something brilliant together
            </h2>
            <p class="preview-p mb-4">
              Whether you have a clear vision or need technical guidance, our
              experts are ready to turn your ideas into functional, beautiful
              realities.
            </p>
            <div class="quick-contact d-flex align-items-center gap-4">
              <a
                href="mailto:hello@yammtech.com"
                class="contact-item text-decoration-none"
              >
                <font-awesome-icon icon="fa-solid fa-envelope" />
                hello@yammtech.com
              </a>
              <a
                href="tel:+1234567890"
                class="contact-item text-decoration-none"
              >
                <font-awesome-icon icon="fa-solid fa-phone" />
                +1 (234) 567-890
              </a>
            </div>
          </div>
          <div class="col-lg-5 text-lg-end">
            <router-link to="/contact" class="preview-cta">
              Quick Inquiry
              <font-awesome-icon icon="fa-solid fa-arrow-right" class="ms-2" />
            </router-link>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import odometer from "odometer";
import "odometer/themes/odometer-theme-default.css";
import { Swiper } from "swiper";
import { Pagination, Autoplay } from "swiper/modules";

export default {
  data() {
    return {
      YTIframeVal: false,
      blogDataLoaded: false,
      teamDataLoaded: true,
      PortfolioDataLoaded: false,
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
      const content = document.querySelector(".homePage");
      const imgload = this.$imagesLoaded(content);
      imgload.on("done", () => {
        this.$nextTick(() => {
          this.$store.dispatch("doneLoading", true);
          this.initSwipers();
          this.initPartnersSwiper();
        });
      });
    },
    initSwiperPort() {
      this.$nextTick(() => {
        // eslint-disable-next-line no-unused-vars
        const portSwiper = new Swiper(this.$refs.portSwiper, {
          modules: [Pagination],
          slidesPerView: 1,
          spaceBetween: 15,
          loop: true,
          centeredSlides: true,
          slidesPerGroup: 1,
          breakpoints: {
            1200: {
              slidesPerView: 2.2,
            },
            576: {
              slidesPerView: 1.4,
            },
          },
          pagination: {
            el: ".swiper-pagination",
            clickable: true,
          },
        });
        this.$ScrollTrigger.refresh();
      });
    },
    initSwiperTeam() {
      this.$nextTick(() => {
        // eslint-disable-next-line no-unused-vars
        const teamSwiper = new Swiper(this.$refs.teamSwiper, {
          modules: [Pagination, Autoplay],
          slidesPerView: 1,
          spaceBetween: 30,
          loop: true,
          autoplay: {
            delay: 3000,
            disableOnInteraction: false,
          },
          grabCursor: true,
          breakpoints: {
            1200: {
              slidesPerView: 4,
            },
            992: {
              slidesPerView: 3,
            },
            768: {
              slidesPerView: 2,
            },
          },
          pagination: {
            el: ".swiper-pagination",
            clickable: true,
          },
        });
        this.$ScrollTrigger.refresh();
      });
    },
    initSwipers() {
      this.$nextTick(() => {
        // eslint-disable-next-line no-unused-vars
        const testimonialsSwiper = new Swiper(this.$refs.testimonialsSwiper, {
          modules: [Pagination, Autoplay],
          slidesPerView: 1,
          spaceBetween: 30,
          loop: true,
          autoplay: {
            delay: 5000,
            disableOnInteraction: false,
          },
          pagination: {
            el: ".swiper-pagination",
            clickable: true,
          },
          breakpoints: {
            992: {
              slidesPerView: 2,
            },
            1200: {
              slidesPerView: 3,
            },
          },
        });
        this.$ScrollTrigger.refresh();
      });
    },
    initPartnersSwiper() {
      this.$nextTick(() => {
        // eslint-disable-next-line no-unused-vars
        const partnersSwiper = new Swiper(this.$refs.partnersSwiper, {
          modules: [Autoplay],
          direction: "vertical",
          slidesPerView: 2,
          spaceBetween: 20,
          loop: true,
          autoplay: {
            delay: 2000,
            disableOnInteraction: false,
          },
          breakpoints: {
            992: {
              slidesPerView: 3,
            },
          },
        });
      });
    },
    getProjectImg(post, index) {
      if (post.imgUrl && post.imgUrl.startsWith("http")) {
        return post.imgUrl;
      }
      // Local fallback mapping based on common project indices/titles
      const localImgs = [
        require("../../imgs/portfolioAssets/portfolio_9.webp"),
        require("../../imgs/portfolioAssets/portfolio_2.webp"),
        require("../../imgs/portfolioAssets/portfolio_3.webp"),
        require("../../imgs/portfolioAssets/portfolio_7.webp"),
        require("../../imgs/portfolioAssets/portfolio_4.webp"),
        require("../../imgs/portfolioAssets/portfolio_1.webp"),
        require("../../imgs/portfolioAssets/portfolio_10.webp"),
      ];
      return localImgs[index % localImgs.length];
    },
    gsapAnimation() {
      const scrollTriggerConfig = (trigger) => ({
        trigger,
        start: "+100 bottom",
        end: "center center",
        scrub: false,
        markers: false,
        toggleActions: "play none none reverse",
      });

      const fadeIn = (target, x = 0, y = 0, duration = 1) => {
        this.$gsap.from(target, {
          x,
          y,
          duration,
          opacity: 0,
          scrollTrigger: scrollTriggerConfig(target),
        });
      };

      this.$gsap.from(".hero .head", {
        x: 100,
        duration: 1,
      });

      fadeIn(".servicesbtn", 50);
      fadeIn(".portfolio .head h1", 0, 50, 0.5);
      fadeIn(".slidOurTeam", 50);

      this.$gsap.from(".choose-item", {
        y: 50,
        opacity: 0,
        duration: 0.8,
        stagger: 0.2,
        scrollTrigger: scrollTriggerConfig(".why-choose-us"),
      });

      this.$gsap
        .timeline({
          scrollTrigger: {
            trigger: ".comments",
            start: "top bottom",
            end: "bottom center",
            scrub: 1.5,
            markers: false,
          },
        })
        .to(".commentsSvg", {
          y: 50,
        });
    },
    nextSwiper(swiperRef) {
      const activeSwiperRefRef = this.$refs[swiperRef];
      activeSwiperRefRef.swiper.slideNext();
    },
    prevSwiper(carouselRef) {
      const activeCarouselRef = this.$refs[carouselRef];
      activeCarouselRef.swiper.slidePrev();
    },
    async teamLoadData() {
      const data = this.$store.getters["teamMembers/teamData"];
      if (data.length !== 4) {
        await this.$store.dispatch("teamMembers/fetchTeammembersData");
      }
      const content = document.querySelector(".ourTeam");
      const imgload = this.$imagesLoaded(content);
      // Fallback timeout
      setTimeout(() => {
        if (!this.teamDataLoaded) {
          this.teamDataLoaded = true;
          this.initSwiperTeam();
        }
      }, 5000);
      imgload.on("always", () => {
        this.teamDataLoaded = true;
        this.initSwiperTeam();
      });
    },
    async getPortfolioData() {
      const data = this.$store.getters["portfolio/projectsData"];
      if (data.length === 0) {
        await this.$store.dispatch("portfolio/homePortfoliosData", "5");
      }
      const content = document.querySelector(".portfolio");
      const imgload = this.$imagesLoaded(content);
      // Fallback timeout
      setTimeout(() => {
        if (!this.PortfolioDataLoaded) {
          this.PortfolioDataLoaded = true;
          this.initSwiperPort();
        }
      }, 5000);
      imgload.on("always", () => {
        this.PortfolioDataLoaded = true;
        this.initSwiperPort();
      });
    },
    odometerInit() {
      const els = document.querySelectorAll(".odometer");
      els.forEach((ele) => {
        new odometer({
          el: ele,
          value: 0,
        });

        this.$ScrollTrigger.create({
          trigger: ele,
          start: "bottom 98%",
          onToggle: () => {
            ele.innerHTML = ele.dataset.numm;
          },
        });
      });
    },
    tiltInit() {
      const elements = document.querySelectorAll(".box-tilt");
      const baseQuery = "(min-width: 992px)";

      const bQMatch = window.matchMedia(baseQuery);

      if (bQMatch.matches) {
        elements.forEach((ele) => {
          this.$VanillaTilt.init(ele);
        });
      }
    },
  },
  computed: {
    getTeamMembersData() {
      return this.$store.getters["teamMembers/teamData"];
    },
    getProjectsData() {
      return this.$store.getters["portfolio/projectsData"];
    },
  },
  async mounted() {
    this.gsapAnimation();
    this.odometerInit();
    this.doneLoading();
    this.teamLoadData();
    this.getPortfolioData();
    this.tiltInit();
  },
  beforeRouteUpdate() {
    this.gsapAnimation();
  },
};
</script>

<style lang="scss" scoped>
/* ALL CSS REMAINS EXACTLY THE SAME - COPY FROM ORIGINAL FILE */
/* CSS ko change nahi kiya, same rakha hai */
.homePage {
  position: relative;
  @media (max-width: 1540px) {
    .hero {
      padding-top: 220px !important;
      min-height: 960px !important;
    }
  }
  @media (max-width: 1150px) and (min-width: 758px) {
    .hero {
      height: initial !important;
    }
  }
  @media (max-width: 1400px) {
    .hero {
      padding-top: 200px !important;
      min-height: 880px !important;
    }
  }
  @media (max-width: 1200px) {
    .hero {
      padding-top: 200px !important;
      padding-bottom: 350px !important;
    }
  }
  @media (max-width: 767px) {
    .hero {
      padding-top: 60px !important;
      padding-bottom: 260px !important;
      min-height: 680px !important;
      display: flex;
      align-items: center;
    }
  }
  .hero {
    background: radial-gradient(
        circle at 0% 0%,
        rgba(31, 81, 254, 0.15) 0%,
        rgba(10, 10, 10, 0) 50%
      ),
      linear-gradient(180deg, #071233 0%, #020510 100%);
    min-height: 100dvh;
    height: auto;
    padding: 220px 0 170px;
    margin-bottom: 200px;
    background-repeat: no-repeat;
    background-attachment: fixed;
    background-size: cover;
    background-position: center;
    position: relative;
    overflow: hidden;
    .content {
      .shape {
        position: absolute;
        border-radius: 50%;
        filter: blur(80px);
        opacity: 0.5;
        animation: shapeAnimation 20s infinite linear;
        z-index: -1;

        &:nth-child(1) {
          width: 300px;
          height: 300px;
          background: rgba(31, 81, 254, 0.3);
          top: -100px;
          left: -100px;
        }
        &:nth-child(2) {
          width: 400px;
          height: 400px;
          background: rgba(255, 196, 46, 0.1);
          bottom: -150px;
          right: -100px;
          animation-duration: 25s;
          animation-direction: reverse;
        }
        &:nth-child(3) {
          width: 250px;
          height: 250px;
          background: rgba(31, 81, 254, 0.2);
          top: 50%;
          left: 50%;
          animation-duration: 15s;
        }
      }

      h1.head {
        font-family: var(--font-heading);
        font-size: 84px;
        font-weight: 800;
        line-height: 1.1;
        margin-bottom: 40px;
        color: var(--text-main);
        letter-spacing: -2px;

        @media (max-width: 1400px) {
          font-size: 72px !important;
        }
        @media (max-width: 1199px) {
          font-size: 64px !important;
        }
        @media (max-width: 991px) {
          font-size: 48px !important;
          margin-bottom: 25px !important;
          letter-spacing: -1px;
        }
        @media (max-width: 575px) {
          font-size: 38px !important;
        }

        span.text-gradient {
          display: block;
          margin-top: 10px;
        }
      }
      .getaQuote {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        gap: 30px;

        @media (max-width: 991px) {
          gap: 25px;
        }

        .hero-btns {
          flex-shrink: 0;
          display: flex;
          gap: 15px;

          .mainBtn {
            box-shadow: 0 10px 20px rgba(255, 196, 46, 0.2);
            &:hover {
              transform: translateY(-3px);
              box-shadow: 0 15px 30px rgba(255, 196, 46, 0.3);
            }
          }

          .secondBtn.basic {
            background-color: transparent;
            border: 1px solid rgba(255, 255, 255, 0.2);
            padding: 10px 27px;
            &:hover {
              background-color: rgba(255, 255, 255, 0.05);
              border-color: rgba(255, 255, 255, 0.4);
              transform: translateY(-3px);
            }
          }
        }

        p {
          max-width: 600px;
          font-size: 18px;
          color: var(--text-muted);
          line-height: 1.6;
          margin: 0;
          font-family: var(--font-body);
        }
      }
      @media (max-width: 1199px) {
        .scrollDown {
          bottom: 220px !important;
        }
      }
      .scrollDown {
        content: "";
        position: absolute;
        height: 35px;
        width: 20px;
        border-radius: 10px;
        border: 2px solid white;
        left: 50%;
        transform: translate(-50%);
        bottom: 25%;
      }

      @media (max-width: 1199px) {
        .scroll-indicator-wrap {
          bottom: 220px !important;
        }
      }

      .hero-trust-indicators {
        margin-top: 50px;
        @media (max-width: 767px) {
          margin-top: 30px;
          gap: 20px !important;
        }
        .trust-item {
          display: flex;
          flex-direction: column;
          gap: 5px;
          .num {
            font-family: var(--font-heading);
            font-size: 32px;
            font-weight: 800;
            color: var(--sec-color);
            line-height: 1;
          }
          .label {
            font-size: 14px;
            text-transform: uppercase;
            letter-spacing: 1px;
            color: var(--text-muted);
            line-height: 1.3;
            font-weight: 600;
          }
        }
      }

      .scroll-indicator-wrap {
        position: absolute;
        bottom: 5%;
        left: 0;
        display: flex;
        align-items: center;
        gap: 15px;
        color: var(--text-muted);
        font-size: 13px;
        font-weight: 700;
        text-transform: uppercase;
        letter-spacing: 2px;

        @media (max-width: 991px) {
          position: relative;
          bottom: 0;
          margin-top: 50px;
        }

        .scroll-mouse {
          width: 22px;
          height: 40px;
          border: 2px solid rgba(255, 255, 255, 0.2);
          border-radius: 20px;
          position: relative;

          .scroll-wheel {
            width: 2px;
            height: 6px;
            background: var(--sec-color);
            position: absolute;
            top: 8px;
            left: 50%;
            transform: translateX(-50%);
            border-radius: 2px;
            animation: scroll-anim 2s infinite;
          }
        }
      }
    }
    @media (max-width: 1200px) {
      .follow-us {
        display: none;
      }
    }
    .follow-us {
      position: absolute;
      top: 50%;
      right: 45px;
      transform: translateY(-85%) rotate(180deg);
      writing-mode: vertical-lr;
      span {
        color: #fefefe;
        display: inline;
        text-transform: capitalize;
        font-size: 17px;
        font-weight: 500;
        position: relative;
        &:not(:last-of-type) {
          padding-bottom: 35px;
        }
        &:nth-child(1) {
          &::after {
            content: "";
            position: absolute;
            right: 50%;
            transform: translate(-50%);
            bottom: 10px;
            height: 15px;
            width: 2px;
            background-color: #fefefe;
          }
        }
        &:nth-child(2) {
          cursor: pointer;
          transition: color 0.3s ease-in-out;
          @media (min-width: 992px) {
            &:hover {
              color: var(--prim-color);
            }
          }
          &::after {
            content: "";
            position: absolute;
            left: 0px;
            bottom: 10px;
            height: 2px;
            width: 15px;
            background-color: #fefefe;
          }
        }
        &:nth-child(3) {
          padding-top: 10px;
          cursor: pointer;
          transition: color 0.3s ease-in-out;
          @media (min-width: 992px) {
            &:hover {
              color: var(--prim-color);
            }
          }
        }
      }
    }
  }
  @media (max-width: 991px) {
    .ourFunFact {
      margin-bottom: 80px !important;
    }
  }
  .ourFunFact {
    margin-bottom: 150px;
    @media (max-width: 1399px) {
      .statusBorder {
        padding: 60px 50px !important;
      }
    }
    @media (max-width: 575px) {
      .statusBorder {
        padding: 40px 30px !important;
      }
    }
    .statusBorder {
      position: relative;
      padding: 60px 80px;
      background: linear-gradient(267.18deg, #161616 0%, #080808 100%);
      border-radius: 15px;
      margin-top: 0;
      z-index: 1;
      overflow: hidden;
      img {
        position: absolute;
        top: 0;
        right: -20%;
        width: 100%;
        height: 100%;
      }
      @media (max-width: 1199px) {
        .status {
          flex-direction: column;
          .info {
            width: 100% !important;
            margin-bottom: 50px !important;
          }
          .nums {
            width: 100% !important;
            padding-left: 0px !important;
          }
        }
      }
      .status {
        display: flex;
        position: relative;
        @media (max-width: 1400px) {
          .info {
            h1 {
              margin-bottom: 10px !important;
              font-size: 42px !important;
            }
          }
        }
        @media (max-width: 991px) {
          .info {
            margin-bottom: 30px !important;
          }
        }
        .info {
          width: 40%;
          h1 {
            font-size: 50px;
            margin-bottom: 20px;
            font-weight: bold;
          }
          p {
            margin: 0;
            color: #fefefeb3;
            line-height: 1.75em;
            font-size: 17px;
          }
        }
        @media (max-width: 1400px) {
          .nums {
            padding-left: 50px !important;
          }
        }
        @media (max-width: 1199px) {
          .nums {
            padding-left: 0px !important;
          }
        }
        .nums {
          width: 60%;
          padding-left: 80px;
          .num {
            display: flex;
            align-items: center;
            @media (max-width: 1400px) {
              .odometer,
              .kword {
                font-size: 42px !important;
              }
            }
            .odo {
              display: flex;
              align-items: center;
              .kword {
                font-size: 50px;
                font-weight: 700;
              }
            }
            .odometer {
              font-size: 50px;
              padding-top: 5px;
              font-weight: 700;
            }
            .title {
              display: flex;
              flex-direction: column;
              justify-content: center;
              align-items: start;
              margin-left: 13px;
              svg {
                color: var(--sec-color);
                font-size: 13px;
              }
              span {
                color: #fefefeb3;
                font-size: 17px;
              }
            }
          }
        }
      }
    }
  }
  .why-choose-us {
    position: relative;
    overflow: hidden;

    .feature-block {
      background: rgba(255, 255, 255, 0.03);
      backdrop-filter: blur(10px);
      border: 1px solid var(--glass-border);
      transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
      position: relative;
      z-index: 1;

      &::before {
        content: "";
        position: absolute;
        inset: 0;
        background: var(--sec-gradient);
        opacity: 0;
        z-index: -1;
        transition: opacity 0.4s ease;
        border-radius: inherit;
      }

      &:hover {
        transform: translateY(-10px);
        border-color: var(--sec-color);
        box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4);

        &::before {
          opacity: 0.05;
        }

        .icon-wrap {
          background: var(--sec-color);
          color: black;
          transform: rotateY(180deg);
        }
      }

      .icon-wrap {
        width: 70px;
        height: 70px;
        background: rgba(255, 255, 255, 0.05);
        border: 1px solid var(--glass-border);
        border-radius: 20px;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 28px;
        color: var(--sec-color);
        transition: all 0.6s ease;
        margin-bottom: 25px;

        svg {
          filter: drop-shadow(0 0 10px rgba(255, 196, 46, 0.3));
        }
      }

      h3 {
        font-family: var(--font-heading);
        font-size: 24px;
        font-weight: 700;
        color: var(--text-main);
        margin-bottom: 15px;
      }

      p {
        color: var(--text-muted);
        font-size: 16px;
        line-height: 1.6;
        margin: 0;
      }
    }
  }

  .services {
    padding: 100px 0;
    position: relative;
    overflow: hidden;

    &::before {
      content: "";
      position: absolute;
      top: 20%;
      right: -10%;
      width: 400px;
      height: 400px;
      background: radial-gradient(
        circle,
        rgba(31, 81, 254, 0.05) 0%,
        transparent 70%
      );
      filter: blur(50px);
      z-index: 0;
    }

    .content {
      position: relative;
      z-index: 1;

      .info {
        @media (max-width: 1199px) {
          margin-bottom: 50px;
          text-align: center;
          display: flex;
          flex-direction: column;
          align-items: center;
        }

        .mainTitle {
          font-family: var(--font-heading);
          font-size: 48px;
          font-weight: 800;
          color: var(--text-main);
          line-height: 1.1;
          margin: 15px 0 35px;

          @media (max-width: 1199px) {
            font-size: 38px;
          }
        }
      }

      .services-grid {
        margin: 0;

        .service-box {
          height: 100%;
          transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
          border: 1px solid rgba(255, 255, 255, 0.05);
          position: relative;
          overflow: hidden;

          &::after {
            content: "";
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(
              90deg,
              transparent,
              rgba(255, 255, 255, 0.05),
              transparent
            );
            transition: 0.6s;
          }

          &:hover {
            transform: translateY(-10px);
            border-color: rgba(255, 196, 46, 0.3);
            background: rgba(255, 255, 255, 0.05);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);

            &::after {
              left: 100%;
            }

            .icon-box {
              background: var(--sec-color);
              .icon-gold {
                color: #000;
                filter: none;
              }
            }

            .learn-more {
              color: var(--sec-color);
              svg {
                transform: translateX(5px);
              }
            }
          }

          .icon-box {
            width: 60px;
            height: 60px;
            background: rgba(255, 196, 46, 0.1);
            border-radius: 16px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            transition: var(--transition);

            .icon-gold {
              color: var(--sec-color);
              transition: var(--transition);
            }
          }

          .title {
            font-family: var(--font-heading);
            font-size: 20px;
            font-weight: 700;
            color: var(--text-main);
            margin-bottom: 12px;
            display: block;
          }

          .desc {
            font-size: 15px;
            line-height: 1.6;
            color: var(--text-muted);
            margin-bottom: 25px;
          }

          .learn-more {
            display: flex;
            align-items: center;
            gap: 10px;
            color: var(--text-main);
            font-size: 14px;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: var(--transition);
            text-decoration: none;

            svg {
              font-size: 12px;
              transition: var(--transition);
            }
          }
        }
      }
    }
  }

  @media (max-width: 991px) {
    .portfolio {
      margin-top: 50px !important;
    }
  }
  .portfolio {
    margin-top: 150px;
    @media (max-width: 991px) {
      margin-top: 80px;
    }

    .content {
      .head {
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        margin-bottom: 70px;
        text-align: center;

        h1 {
          font-family: var(--font-heading);
          font-size: 54px;
          font-weight: 800;
          color: var(--text-main);
          margin-top: 10px;

          @media (max-width: 1199px) {
            font-size: 44px;
          }
          @media (max-width: 991px) {
            font-size: 34px;
          }
        }
      }

      .swiper-container {
        padding: 40px 0;

        .swiper-wrapper {
          .swiper-slide {
            padding: 20px;

            .slide {
              height: 480px;
              width: 100%;
              border-radius: 24px;
              overflow: hidden;
              position: relative;
              background: #111;
              box-shadow: var(--shadow-premium);
              transition: var(--transition);

              @media (max-width: 991px) {
                height: 380px;
              }

              .img {
                width: 100%;
                height: 100%;
                position: relative;

                img {
                  width: 100%;
                  height: 100%;
                  object-fit: cover;
                  transition: transform 0.6s cubic-bezier(0.4, 0, 0.2, 1);
                }

                .overlay {
                  position: absolute;
                  top: 0;
                  left: 0;
                  width: 100%;
                  height: 100%;
                  background: linear-gradient(
                    to top,
                    rgba(0, 0, 0, 0.9) 0%,
                    rgba(0, 0, 0, 0.2) 50%,
                    transparent 100%
                  );
                  display: flex;
                  align-items: flex-end;
                  padding: 40px;
                  opacity: 0;
                  transition: all 0.4s ease;
                  z-index: 2;

                  .project-info {
                    transform: translateY(20px);
                    transition: all 0.4s ease;

                    .category {
                      color: var(--sec-color);
                      font-size: 14px;
                      font-weight: 600;
                      text-transform: uppercase;
                      letter-spacing: 2px;
                      display: block;
                      margin-bottom: 8px;
                    }

                    .title {
                      color: #fff;
                      font-size: 28px;
                      font-weight: 700;
                      margin-bottom: 20px;
                      font-family: var(--font-heading);
                    }

                    .view-btn {
                      display: flex;
                      align-items: center;
                      gap: 10px;
                      color: #fff;
                      font-weight: 600;
                      font-size: 15px;

                      svg {
                        transition: transform 0.3s ease;
                      }
                    }
                  }
                }

                @media (min-width: 992px) {
                  &:hover {
                    img {
                      transform: scale(1.1);
                    }
                    .overlay {
                      opacity: 1;
                      .project-info {
                        transform: translateY(0);
                      }
                    }
                    .view-btn svg {
                      transform: translateX(5px);
                    }
                  }
                }

                @media (max-width: 991px) {
                  .overlay {
                    opacity: 1;
                    padding: 20px;
                    .project-info {
                      transform: translateY(0);
                      .title {
                        font-size: 20px;
                        margin-bottom: 10px;
                      }
                    }
                  }
                }
              }
            }
          }
        }
      }
    }

    .ourTeam {
      margin-bottom: 150px;

      .team-text-slider {
        padding: 50px 0;

        .memberCard {
          background: rgba(255, 255, 255, 0.03);
          backdrop-filter: blur(10px);
          border: 1px solid var(--glass-border);
          border-radius: 20px;
          padding: 50px 30px;
          transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
          height: 100%;
          min-height: 280px;
          display: flex;
          flex-direction: column;
          align-items: center;
          justify-content: center;
          position: relative;
          z-index: 1;

          &::after {
            content: "";
            position: absolute;
            inset: 0;
            border-radius: 20px;
            padding: 2px;
            background: linear-gradient(
              45deg,
              transparent,
              var(--sec-color),
              transparent
            );
            -webkit-mask: linear-gradient(#fff 0 0) content-box,
              linear-gradient(#fff 0 0);
            mask: linear-gradient(#fff 0 0) content-box,
              linear-gradient(#fff 0 0);
            -webkit-mask-composite: xor;
            mask-composite: exclude;
            opacity: 0;
            transition: opacity 0.4s ease;
          }

          &:hover {
            background: rgba(255, 255, 255, 0.07);
            border-color: rgba(255, 255, 255, 0.1);
            transform: translateY(-15px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4);

            &::after {
              opacity: 1;
            }

            .name {
              color: var(--sec-color);
            }
          }

          .name {
            font-family: var(--font-heading);
            font-size: 28px;
            font-weight: 800;
            color: var(--text-main);
            margin-bottom: 12px;
            transition: color 0.3s ease;
          }

          .expertise {
            color: var(--text-muted);
            font-size: 14px;
            text-transform: uppercase;
            letter-spacing: 2px;
            font-weight: 600;
            margin-bottom: 25px;
          }

          .socials {
            display: flex;
            gap: 15px;

            .social {
              width: 42px;
              height: 42px;
              background: rgba(255, 255, 255, 0.05);
              border: 1px solid rgba(255, 255, 255, 0.1);
              border-radius: 50%;
              display: flex;
              align-items: center;
              justify-content: center;
              color: var(--text-main);
              transition: all 0.3s ease;

              &:hover {
                background: var(--sec-color);
                color: #000;
                border-color: var(--sec-color);
                transform: rotate(360deg);
              }
            }
          }
        }
      }
    }

    .comments {
      padding: 130px 0;
      background: linear-gradient(180deg, #0a0a0a 0%, #080808 100%);
      position: relative;
      overflow: hidden;

      &::before {
        content: "";
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        height: 1px;
        background: linear-gradient(
          90deg,
          transparent,
          var(--sec-color),
          transparent
        );
        opacity: 0.3;
      }

      .testimonials-swiper {
        padding: 50px 0 80px;

        .swiper-slide {
          height: auto;
        }
      }

      .testimonial-card {
        background: rgba(255, 255, 255, 0.03);
        backdrop-filter: blur(20px);
        -webkit-backdrop-filter: blur(20px);
        border: 1px solid rgba(255, 255, 255, 0.08);
        border-radius: 20px;
        padding: 25px;
        height: 100%;
        position: relative;
        transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
        overflow: hidden;
        display: flex;
        flex-direction: column;

        &::before {
          content: "";
          position: absolute;
          top: 0;
          left: 0;
          width: 100%;
          height: 100%;
          background: radial-gradient(
            circle at top right,
            rgba(255, 196, 46, 0.06),
            transparent 60%
          );
          pointer-events: none;
        }

        &:hover {
          border-color: rgba(255, 196, 46, 0.3);
          transform: translateY(-5px);
          background: rgba(255, 255, 255, 0.05);

          .client-photo {
            border-color: var(--sec-color);
          }

          .quote-bg {
            opacity: 0.1;
            transform: scale(1.1);
          }
        }

        .client-photo {
          width: 50px;
          height: 50px;
          border-radius: 50%;
          overflow: hidden;
          margin-bottom: 15px;
          border: 2px solid rgba(255, 255, 255, 0.1);
          transition: all 0.4s ease;

          img {
            width: 100%;
            height: 100%;
            object-fit: cover;
          }
        }

        .stars {
          margin-bottom: 12px;
          display: flex;
          gap: 3px;

          svg {
            color: var(--sec-color);
            font-size: 10px;
            filter: drop-shadow(0 0 5px rgba(255, 196, 46, 0.3));
            &.deactive {
              color: rgba(254, 254, 254, 0.1);
              filter: none;
            }
          }
        }

        .review {
          font-size: 14px;
          font-weight: 400;
          line-height: 1.6;
          color: rgba(255, 255, 255, 0.8);
          margin-bottom: 20px;
          font-style: italic;
          position: relative;
          z-index: 1;
          flex-grow: 1;
        }

        .client-info {
          position: relative;
          z-index: 1;
          border-top: 1px solid rgba(255, 255, 255, 0.06);
          padding-top: 15px;

          .name {
            font-family: var(--font-heading);
            font-size: 16px;
            font-weight: 700;
            color: var(--text-main);
            margin: 0;
          }

          .role {
            color: var(--sec-color);
            font-size: 10px;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1.2px;
            margin-top: 3px;
            display: block;
            opacity: 0.7;
          }
        }

        .quote-bg {
          position: absolute;
          bottom: 15px;
          right: 15px;
          font-size: 40px;
          color: var(--sec-color);
          opacity: 0.03;
          transform: rotate(10deg);
          transition: all 0.5s ease;
          pointer-events: none;
        }
      }

      .swiper-pagination {
        bottom: 20px;
        .swiper-pagination-bullet {
          background: var(--sec-color);
          opacity: 0.3;
          &-active {
            opacity: 1;
            width: 25px;
            border-radius: 10px;
          }
        }
      }
    }

    .partners {
      background: rgba(255, 255, 255, 0.02);
      border-top: 1px solid var(--glass-border);
      border-bottom: 1px solid var(--glass-border);
      padding: 60px 0;

      .partners-slider {
        width: 100%;
        height: 350px;
        padding: 10px 0;
        margin: 0 auto;
        max-width: 250px;

        .swiper-slide {
          display: flex;
          align-items: center;
          justify-content: center;
          transition: all 0.3s ease;
          opacity: 0.5;

          &:hover {
            opacity: 1;
            transform: scale(1.05);
          }

          img {
            max-width: 150px;
            width: 100%;
            height: auto;
            filter: grayscale(1) brightness(2);
            transition: all 0.4s ease;

            &:hover {
              filter: grayscale(0) brightness(1);
            }
          }
        }
      }

      .partners-info {
        h2 {
          font-family: var(--font-heading);
          font-weight: 800;
          font-size: 36px;
        }
        p {
          font-size: 18px;
          line-height: 1.6;
        }
      }
    }
    .meeting {
      @media (max-width: 991px) {
        .content {
          padding: 70px 30px !important;
        }
      }
      @media (max-width: 575px) {
        .content {
          padding: 70px 20px !important;
        }
      }
      .content {
        position: relative;
        background: linear-gradient(267.18deg, #161616 0%, #080808 100%);
        padding: 90px 30px;
        border-radius: 15px;
        text-align: center;
        overflow: hidden;
        .shape {
          z-index: 2 !important;
        }
        .mainTitle {
          position: relative;
          z-index: 3;
        }
        .statusSvg {
          position: absolute;
          top: 0;
          right: 0;
          width: 100%;
          height: 100%;
          z-index: 1;
        }
        @media (max-width: 575px) {
          .mainTitle {
            font-size: 28px !important;
          }
        }
        @media (max-width: 991px) {
          .meetingBtn {
            margin: 30px auto 0 !important;
          }
        }
        .meetingBtn {
          position: relative;
          margin: 70px auto 0;
          z-index: 3;
        }
      }
    }
  }

  @keyframes scrolldown {
    0% {
      top: 30%;
      opacity: 1;
      width: 5px;
      height: 5px;
    }
    50% {
      top: 70%;
      opacity: 0.5;
      width: 4px;
      height: 4px;
    }
    100% {
      top: 30%;
      opacity: 1;
      width: 5px;
      height: 5px;
    }
  }
  @keyframes arrowShapeAnimation {
    0% {
      transform: translate(0, -50%) rotate(45deg);
    }
    50% {
      transform: translate(60px, -50%) rotate(45deg);
    }
    100% {
      transform: translate(0, -50%) rotate(45deg);
    }
  }
  @keyframes playBtnAnimation {
    0% {
    }
    100% {
      transform: scale(1.5);
      opacity: 0;
    }
  }
  @keyframes scrollerAnimation {
    to {
      transform: translate(calc(-50% - 12px));
    }
  }
  @keyframes enterportSlidesAnimation {
    from {
      bottom: -200px;
      left: -100px;
      opacity: 0;
    }
    to {
      bottom: -60px;
      left: -40px;
      opacity: 1;
    }
  }
  @keyframes enterspanPortSlidesAnimation {
    from {
      left: 50px;
      opacity: 0;
    }
    to {
      left: 0;
      opacity: 1;
    }
  }
  @keyframes leaveportSlidesAnimation {
    from {
      bottom: -60px;
      left: -40px;
      opacity: 1;
    }
    to {
      bottom: -200px;
      left: -100px;
      opacity: 0;
    }
  }
  @keyframes leavespanPortSlidesAnimation {
    from {
      left: 0;
      opacity: 1;
    }
    to {
      left: 50px;
      opacity: 0;
    }
  }
  .YTIframe-enter-active,
  .YTIframe-leave-active {
    transition-duration: 0.5s;
  }

  .YTIframe-enter-from,
  .YTIframe-leave-to {
    opacity: 0;
    transform: translateY(-50px);
  }
  .YTIframe-enter-to {
    opacity: 1;
    transform: translateY(0);
  }
  .cta-section {
    padding: 100px 0;
    .cta-content {
      border: 1px solid var(--glass-border);
      background: rgba(255, 255, 255, 0.03);
      backdrop-filter: blur(20px);
      border-radius: 30px;

      .cta-title {
        font-family: var(--font-heading);
        font-size: 48px;
        font-weight: 800;
        color: var(--text-main);
        margin-bottom: 20px;
        @media (max-width: 767px) {
          font-size: 32px;
        }
      }

      .cta-desc {
        font-size: 18px;
        color: var(--text-muted);
        max-width: 700px;
        margin: 0 auto 40px;
        line-height: 1.6;
      }

      .shape {
        position: absolute;
        border-radius: 50%;
        filter: blur(80px);
        opacity: 0.5;
        animation: shapeAnimation 20s infinite linear;
        z-index: -1;

        &:nth-child(1) {
          width: 300px;
          height: 300px;
          background: rgba(31, 81, 254, 0.3);
          top: -100px;
          left: -100px;
        }
        &:nth-child(2) {
          width: 400px;
          height: 400px;
          background: rgba(255, 196, 46, 0.1);
          bottom: -150px;
          right: -100px;
          animation-duration: 25s;
          animation-direction: reverse;
        }
      }
    }
  }

  .contact-preview {
    background: rgba(0, 0, 0, 0.2);
    border-top: 1px solid var(--glass-border);
    padding: 80px 0;

    .section-title {
      font-family: var(--font-heading);
      font-size: 42px;
      font-weight: 800;
      color: var(--text-main);
      margin-bottom: 20px;
      @media (max-width: 767px) {
        font-size: 32px;
      }
    }

    .preview-p {
      color: var(--text-muted);
      font-size: 16px;
      line-height: 1.7;
    }

    .quick-contact {
      .contact-item {
        display: flex;
        align-items: center;
        gap: 10px;
        color: var(--text-main);
        font-weight: 600;
        font-size: 15px;

        svg {
          color: var(--sec-color);
        }
      }
      @media (max-width: 575px) {
        flex-direction: column;
        gap: 15px !important;
      }
    }

    .preview-cta {
      display: inline-flex;
      align-items: center;
      gap: 15px;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 1px;
      color: var(--text-main);
      font-size: 16px;
      padding: 15px 30px;
      border: 1px solid rgba(255, 255, 255, 0.1);
      border-radius: 50px;
      transition: all 0.3s ease;
      text-decoration: none;

      svg {
        transition: transform 0.3s ease;
      }

      &:hover {
        background: var(--sec-color);
        color: black;
        border-color: var(--sec-color);
        transform: translateY(-5px);

        svg {
          transform: translateX(5px);
        }
      }
    }
  }

  @keyframes scroll-anim {
    0% {
      opacity: 1;
      transform: translateX(-50%) translateY(0);
    }
    100% {
      opacity: 0;
      transform: translateX(-50%) translateY(15px);
    }
  }

  @keyframes scroll-mouse-anim {
    0% {
      transform: translateY(0);
    }
    50% {
      transform: translateY(5px);
    }
    100% {
      transform: translateY(0);
    }
  }

  @keyframes shapeAnimation {
    0% {
      transform: translate(0, 0) scale(1);
    }
    33% {
      transform: translate(30px, -50px) scale(1.1);
    }
    66% {
      transform: translate(-20px, 20px) scale(0.9);
    }
    100% {
      transform: translate(0, 0) scale(1);
    }
  }
}

.dataFadein-enter-active,
.dataFadein-leave-active {
  transition-duration: 1s;
}

.dataFadein-enter-from,
.dataFadein-leave-to {
  opacity: 0;
}
.dataFadein-enter-to {
  opacity: 1;
}
</style>
