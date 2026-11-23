<template>
  <main class="home-page">
    <!-- HERO -->
    <section class="hero section-cutout">
      <div class="hero-content">
        <span class="eyebrow">
          Beauty • Creative Direction • Artistry
        </span>

        <h1>
          Creative expression,
          <span>beautifully directed.</span>
        </h1>

        <p>
          Chelby Arts brings beauty, creativity and visual direction together
          to create refined, expressive experiences for individuals, brands
          and special moments.
        </p>

        <div class="hero-actions">
          <RouterLink to="/portfolio" class="primary-btn">
            View Our Work
          </RouterLink>

          <RouterLink to="/contact" class="secondary-btn">
            Book a Consultation
          </RouterLink>
        </div>
      </div>

      <div class="hero-art">
        <div class="art-card">
          <img src="@/assets/chelbylogo.svg" alt="Chelby Arts" />
        </div>

        <div class="art-circle art-circle-one"></div>
        <div class="art-circle art-circle-two"></div>

        <div class="floating-tag tag-one">
          Beauty
        </div>

        <div class="floating-tag tag-two">
          Creative Direction
        </div>
      </div>
    </section>

    <!-- ABOUT -->
    <section class="intro-section section-cutout">
      <div class="intro-label">
        <span>01</span>
        <p>About Chelby Arts</p>
      </div>

      <div class="intro-content">
        <h2>
          Artistry with intention.
          <span>Creativity with identity.</span>
        </h2>

        <p>
          We create thoughtful beauty and creative experiences that feel
          elevated, personal and visually distinct. Every concept is shaped
          around your individuality, story and desired aesthetic.
        </p>

        <RouterLink to="/about" class="text-link">
          Discover our story
          <span>→</span>
        </RouterLink>
      </div>
    </section>

    <!-- SERVICES -->
    <section class="services-section section-cutout">
      <div class="section-heading">
        <div>
          <span class="eyebrow">
            What We Do
          </span>

          <h2>
            Our creative services
          </h2>
        </div>

        <RouterLink to="/services" class="text-link">
          View all services
          <span>→</span>
        </RouterLink>
      </div>

      <div class="services-grid">
        <article class="service-card">
          <span class="service-number">01</span>

          <div class="service-content">
            <span class="service-tag">Beauty</span>

            <h3>Beauty Artistry</h3>

            <p>
              Refined beauty looks tailored to your features, personality and
              occasion.
            </p>

            <RouterLink to="/services" class="service-link">
              Explore
              <span>↗</span>
            </RouterLink>
          </div>
        </article>

        <article class="service-card service-card-featured">
          <span class="service-number">02</span>

          <div class="service-content">
            <span class="service-tag">Creative</span>

            <h3>Creative Direction</h3>

            <p>
              Visual concepts, styling and creative direction for brands,
              campaigns and personal projects.
            </p>

            <RouterLink to="/services" class="service-link">
              Explore
              <span>↗</span>
            </RouterLink>
          </div>
        </article>

        <article class="service-card">
          <span class="service-number">03</span>

          <div class="service-content">
            <span class="service-tag">Visual</span>

            <h3>Editorial Concepts</h3>

            <p>
              Concept-led visual storytelling created for shoots, events and
              artistic collaborations.
            </p>

            <RouterLink to="/services" class="service-link">
              Explore
              <span>↗</span>
            </RouterLink>
          </div>
        </article>
      </div>
    </section>

    <!-- PORTFOLIO -->
    <section class="portfolio-section section-cutout">
      <div class="portfolio-heading">
        <span class="eyebrow">
          Selected Work
        </span>

        <h2>
          Where beauty meets
          <span>creative expression.</span>
        </h2>
      </div>

      <div class="portfolio-grid">
        <RouterLink to="/portfolio" class="portfolio-item portfolio-large">
          <div class="portfolio-placeholder">
            <span>01</span>
          </div>

          <div class="portfolio-info">
            <div>
              <p>Beauty Editorial</p>
              <h3>Soft Form</h3>
            </div>

            <span class="portfolio-arrow">↗</span>
          </div>
        </RouterLink>

        <RouterLink to="/portfolio" class="portfolio-item">
          <div class="portfolio-placeholder portfolio-placeholder-pink">
            <span>02</span>
          </div>

          <div class="portfolio-info">
            <div>
              <p>Creative Direction</p>
              <h3>Modern Muse</h3>
            </div>

            <span class="portfolio-arrow">↗</span>
          </div>
        </RouterLink>

        <RouterLink to="/portfolio" class="portfolio-item">
          <div class="portfolio-placeholder portfolio-placeholder-blue">
            <span>03</span>
          </div>

          <div class="portfolio-info">
            <div>
              <p>Visual Styling</p>
              <h3>Quiet Luxury</h3>
            </div>

            <span class="portfolio-arrow">↗</span>
          </div>
        </RouterLink>
      </div>
    </section>

    <!-- CTA -->
    <section class="cta-section section-cutout">
      <div class="cta-logo">
        <img src="@/assets/chelbylogo.svg" alt="Chelby Arts" />
      </div>

      <div class="cta-content">
        <span class="eyebrow">
          Let’s Create
        </span>

        <h2>
          Have an idea?
          <span>Let’s bring it to life.</span>
        </h2>

        <p>
          Whether you're planning a beauty look, creative project or visual
          concept, we’d love to hear about it.
        </p>

        <RouterLink to="/contact" class="primary-btn">
          Start a Project
        </RouterLink>
      </div>
    </section>
  </main>
</template>

<style scoped lang="scss">
.home-page {
  width: 100%;
  height: 100vh;
  overflow-x: hidden;
  overflow-y: auto;

  background: #ffffff;
  color: #102b53;

  scroll-snap-type: y mandatory;
  scroll-behavior: smooth;
  overscroll-behavior-y: contain;

  -webkit-overflow-scrolling: touch;

  @media (max-width: 767px) {
    height: 100svh;
    scroll-snap-type: y mandatory;
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    height: 100vh;
    scroll-snap-type: y mandatory;
  }

  @media (min-width: 1200px) {
    height: 100vh;
    scroll-snap-type: y mandatory;
  }
}

/* =========================================================
   GLOBAL SECTION SNAP + LOGO CUTOUT
========================================================= */

.section-cutout {
  width: 100%;
  height: 100vh;
  min-height: 100vh;

  position: relative;
  box-sizing: border-box;
  flex-shrink: 0;

  scroll-snap-align: start;
  scroll-snap-stop: always;

  clip-path: polygon(180px 0,
      100% 0,
      100% 100%,
      0 100%,
      0 180px,
      180px 180px);

  @media (max-width: 767px) {
    height: 100svh;
    min-height: 100svh;
    max-height: 100svh;

    clip-path: polygon(90px 0,
        100% 0,
        100% 100%,
        0 100%,
        0 90px,
        90px 90px);
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    height: 100vh;
    min-height: 100vh;

    clip-path: polygon(150px 0,
        100% 0,
        100% 100%,
        0 100%,
        0 150px,
        150px 150px);
  }

  @media (min-width: 1200px) {
    height: 100vh;
    min-height: 100vh;

    clip-path: polygon(180px 0,
        100% 0,
        100% 100%,
        0 100%,
        0 180px,
        180px 180px);
  }
}

/* =========================================================
   HERO
========================================================= */

.hero {
  height: 100vh;
  min-height: 100vh;

  padding: 180px 7% 80px;

  display: grid;
  grid-template-columns: minmax(0, 1fr) minmax(420px, 0.85fr);
  align-items: center;
  gap: 70px;

  box-sizing: border-box;
  overflow: hidden;

  background:
    radial-gradient(circle at 80% 25%,
      rgba(193, 216, 245, 0.24),
      transparent 34%),
    radial-gradient(circle at 65% 70%,
      rgba(247, 207, 213, 0.24),
      transparent 30%),
    #fffdfd;

  @media (max-width: 767px) {
    height: 100svh;
    min-height: 100svh;

    padding:
      104px 20px max(22px, env(safe-area-inset-bottom));

    grid-template-columns: 1fr;
    grid-template-rows: auto minmax(0, 1fr);

    align-content: center;
    align-items: center;

    gap: 18px;
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    padding: 150px 5% 70px;

    grid-template-columns: 1fr 0.8fr;
    gap: 40px;
  }

  @media (min-width: 1200px) {
    padding: 180px 7% 80px;
  }
}

.hero-content {
  max-width: 720px;

  position: relative;
  z-index: 2;

  h1 {
    margin: 22px 0 24px;

    font-size: clamp(3.8rem, 6vw, 7rem);
    line-height: 0.98;

    font-weight: 400;
    letter-spacing: -0.055em;

    span {
      display: block;

      color: #d9a9b5;

      font-style: italic;
      font-weight: 300;
    }
  }

  p {
    max-width: 590px;
    margin: 0;

    color: #667085;

    font-size: 1.08rem;
    line-height: 1.8;
  }

  @media (max-width: 767px) {
    width: 100%;
    max-width: 100%;

    h1 {
      margin: 12px 0 14px;

      font-size: clamp(2.55rem, 11.8vw, 3.65rem);
      line-height: 0.97;

      letter-spacing: -0.05em;
    }

    p {
      max-width: 100%;

      font-size: 0.86rem;
      line-height: 1.5;
    }
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    h1 {
      font-size: clamp(4rem, 7vw, 5.6rem);
    }
  }

  @media (min-width: 1200px) {
    h1 {
      font-size: clamp(5rem, 6vw, 7.4rem);
    }
  }
}

/* =========================================================
   EYEBROW
========================================================= */

.eyebrow {
  display: inline-flex;
  align-items: center;
  gap: 10px;

  color: #102b53;

  font-size: 0.78rem;
  font-weight: 600;

  letter-spacing: 0.2em;
  text-transform: uppercase;

  &::before {
    content: "";

    width: 32px;
    height: 1px;

    flex-shrink: 0;

    background: currentColor;
  }

  @media (max-width: 767px) {
    gap: 7px;

    font-size: 0.6rem;
    letter-spacing: 0.11em;
    line-height: 1.4;

    &::before {
      width: 20px;
    }
  }
}

/* =========================================================
   HERO ACTIONS
========================================================= */

.hero-actions {
  margin-top: 38px;

  display: flex;
  align-items: center;

  gap: 15px;
  flex-wrap: wrap;

  @media (max-width: 767px) {
    width: 100%;
    margin-top: 18px;

    display: grid;
    grid-template-columns: 1fr 1fr;

    gap: 8px;
  }
}

.primary-btn,
.secondary-btn {
  min-height: 52px;
  padding: 0 28px;

  display: inline-flex;
  align-items: center;
  justify-content: center;

  border-radius: 999px;

  text-decoration: none;

  font-size: 0.92rem;
  font-weight: 500;

  transition:
    transform 0.25s ease,
    background 0.25s ease,
    border-color 0.25s ease;

  @media (max-width: 767px) {
    width: 100%;
    min-height: 43px;

    box-sizing: border-box;

    padding: 0 12px;

    font-size: 0.76rem;
  }
}

.primary-btn {
  background: #102b53;
  border: 1px solid #102b53;

  color: #ffffff;

  &:hover {
    transform: translateY(-2px);

    background: #1c3c6a;
  }
}

.secondary-btn {
  border: 1px solid rgba(16, 43, 83, 0.22);

  color: #102b53;

  &:hover {
    border-color: #102b53;

    background: rgba(16, 43, 83, 0.04);
  }
}

/* =========================================================
   HERO ART
========================================================= */

.hero-art {
  min-height: 500px;

  display: flex;
  align-items: center;
  justify-content: center;

  position: relative;
  z-index: 2;

  @media (max-width: 767px) {
    width: 100%;
    height: 100%;
    min-height: 0;

    display: flex;
    align-items: center;
    justify-content: center;
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    min-height: 440px;
  }

  @media (min-width: 1200px) {
    min-height: 520px;
  }
}

.art-card {
  width: min(420px, 80%);
  aspect-ratio: 0.8;

  display: flex;
  align-items: center;
  justify-content: center;

  position: relative;
  z-index: 2;

  background:
    linear-gradient(145deg,
      rgba(217, 169, 181, 0.17),
      rgba(193, 216, 245, 0.22));

  border-radius:
    48% 48% 46% 54% / 42% 42% 58% 58%;

  box-shadow:
    0 35px 80px rgba(16, 43, 83, 0.08);

  img {
    width: 72%;
    height: 72%;

    display: block;

    object-fit: contain;
  }

  @media (max-width: 767px) {
    width: min(170px, 47vw);

    img {
      width: 67%;
      height: 67%;
    }
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    width: min(350px, 88%);
  }

  @media (min-width: 1200px) {
    width: min(430px, 82%);
  }
}

.art-circle {
  position: absolute;

  border-radius: 50%;

  z-index: 1;
}

.art-circle-one {
  width: 180px;
  height: 180px;

  top: 6%;
  right: 4%;

  background: rgba(193, 216, 245, 0.35);

  @media (max-width: 767px) {
    width: 78px;
    height: 78px;

    top: 5%;
    right: 14%;
  }
}

.art-circle-two {
  width: 130px;
  height: 130px;

  bottom: 4%;
  left: 2%;

  border: 1px solid rgba(217, 169, 181, 0.5);

  @media (max-width: 767px) {
    width: 60px;
    height: 60px;

    left: 15%;
    bottom: 4%;
  }
}

.floating-tag {
  padding: 11px 16px;

  position: absolute;
  z-index: 3;

  background: rgba(255, 255, 255, 0.9);

  border: 1px solid rgba(16, 43, 83, 0.08);
  border-radius: 999px;

  box-shadow:
    0 14px 30px rgba(16, 43, 83, 0.08);

  color: #102b53;

  font-size: 0.78rem;
  letter-spacing: 0.08em;

  white-space: nowrap;

  backdrop-filter: blur(12px);

  @media (max-width: 767px) {
    padding: 6px 9px;

    font-size: 0.54rem;
  }
}

.tag-one {
  top: 25%;
  left: 0;

  @media (max-width: 767px) {
    top: 18%;
    left: 9%;
  }
}

.tag-two {
  right: -2%;
  bottom: 24%;

  @media (max-width: 767px) {
    right: 7%;
    bottom: 18%;
  }
}

/* =========================================================
   ABOUT
========================================================= */

.intro-section {
  height: 100vh;
  min-height: 100vh;

  padding: 200px 8% 90px;

  display: grid;
  grid-template-columns: 0.38fr 1fr;

  align-items: center;

  gap: 80px;

  box-sizing: border-box;
  overflow: hidden;

  background: #102b53;
  color: #ffffff;

  @media (max-width: 767px) {
    height: 100svh;
    min-height: 100svh;

    padding:
      105px 20px max(32px, env(safe-area-inset-bottom));

    grid-template-columns: 1fr;
    grid-template-rows: auto 1fr;

    align-content: center;

    gap: 26px;
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    padding: 170px 6% 80px;

    gap: 50px;
  }

  @media (min-width: 1200px) {
    padding: 200px 8% 90px;
  }
}

.intro-label {
  display: flex;
  align-items: flex-start;

  gap: 18px;

  span {
    color: #d9a9b5;

    font-size: 0.8rem;
  }

  p {
    margin: 0;

    color: rgba(255, 255, 255, 0.6);

    font-size: 0.78rem;

    letter-spacing: 0.16em;
    text-transform: uppercase;
  }

  @media (max-width: 767px) {
    gap: 10px;

    span,
    p {
      font-size: 0.64rem;
    }
  }
}

.intro-content {
  max-width: 850px;

  h2 {
    margin: 0;

    font-size: clamp(2.8rem, 5vw, 5rem);
    line-height: 1.05;

    font-weight: 300;

    letter-spacing: -0.04em;

    span {
      display: block;

      color: #d9a9b5;

      font-style: italic;
    }
  }

  p {
    max-width: 680px;

    margin: 30px 0;

    color: rgba(255, 255, 255, 0.72);

    font-size: 1.02rem;
    line-height: 1.85;
  }

  .text-link {
    color: #ffffff;
  }

  @media (max-width: 767px) {
    align-self: center;

    h2 {
      font-size: clamp(2.4rem, 10.5vw, 3.5rem);
      line-height: 1.02;
    }

    p {
      margin: 20px 0;

      font-size: 0.88rem;
      line-height: 1.55;
    }
  }
}

/* =========================================================
   TEXT LINKS
========================================================= */

.text-link {
  display: inline-flex;
  align-items: center;

  gap: 12px;

  color: #102b53;

  text-decoration: none;

  font-size: 0.9rem;
  font-weight: 500;

  span {
    transition: transform 0.25s ease;
  }

  &:hover {
    span {
      transform: translateX(5px);
    }
  }

  @media (max-width: 767px) {
    font-size: 0.8rem;
  }
}

/* =========================================================
   SERVICES
========================================================= */

.services-section {
  height: 100vh;
  min-height: 100vh;

  padding: 200px 8% 80px;

  display: flex;
  flex-direction: column;
  justify-content: center;

  box-sizing: border-box;
  overflow: hidden;

  background: #fffdfd;

  @media (max-width: 767px) {
    height: 100svh;
    min-height: 100svh;
    max-height: 100svh;

    padding:
      105px 20px max(28px, env(safe-area-inset-bottom));

    justify-content: flex-start;
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    padding: 170px 6% 80px;
  }

  @media (min-width: 1200px) {
    padding: 200px 8% 80px;
  }
}

.section-heading {
  margin-bottom: 45px;

  display: flex;
  align-items: flex-end;
  justify-content: space-between;

  gap: 30px;

  h2 {
    margin: 15px 0 0;

    font-size: clamp(2.7rem, 4vw, 4.5rem);

    font-weight: 300;
    letter-spacing: -0.04em;
  }

  @media (max-width: 767px) {
    flex: 0 0 auto;

    margin-bottom: 22px;

    flex-direction: row;
    align-items: flex-end;

    gap: 15px;

    h2 {
      margin-top: 8px;

      font-size: clamp(2rem, 8.5vw, 2.8rem);
      line-height: 1;
    }

    .text-link {
      flex-shrink: 0;

      font-size: 0.72rem;
    }
  }
}

.services-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);

  border-top: 1px solid rgba(16, 43, 83, 0.12);
  border-bottom: 1px solid rgba(16, 43, 83, 0.12);

  @media (max-width: 767px) {
    width: calc(100% + 20px);

    margin-right: -20px;

    flex: 1;
    min-height: 0;

    display: flex;

    gap: 12px;

    overflow-x: auto;
    overflow-y: hidden;

    padding-right: 20px;
    padding-bottom: 8px;

    border: none;

    scroll-snap-type: x mandatory;

    -webkit-overflow-scrolling: touch;
    scrollbar-width: none;

    &::-webkit-scrollbar {
      display: none;
    }
  }
}

.service-card {
  min-height: 330px;

  padding: 30px;

  display: flex;
  flex-direction: column;
  justify-content: space-between;

  box-sizing: border-box;

  border-right: 1px solid rgba(16, 43, 83, 0.12);

  position: relative;
  overflow: hidden;

  transition:
    background 0.3s ease,
    color 0.3s ease;

  &:last-child {
    border-right: none;
  }

  &:hover {
    background: #102b53;
    color: #ffffff;

    p,
    .service-number,
    .service-tag {
      color: rgba(255, 255, 255, 0.7);
    }

    .service-link {
      color: #ffffff;
    }
  }

  @media (max-width: 767px) {
    width: 78vw;
    min-width: 78vw;

    height: 100%;
    min-height: 0;

    padding: 22px;

    border: 1px solid rgba(16, 43, 83, 0.1);
    border-radius: 20px;

    background: #ffffff;

    scroll-snap-align: start;

    &:last-child {
      border: 1px solid rgba(16, 43, 83, 0.1);
    }
  }
}

.service-card-featured {
  background: rgba(217, 169, 181, 0.12);
}

.service-number {
  color: #98a2b3;

  font-size: 0.75rem;

  @media (max-width: 767px) {
    font-size: 0.68rem;
  }
}

.service-content {
  h3 {
    margin: 12px 0 16px;

    font-size: 2rem;
    font-weight: 400;
  }

  p {
    max-width: 320px;

    margin: 0 0 30px;

    color: #667085;

    line-height: 1.7;
  }

  @media (max-width: 767px) {
    h3 {
      margin: 9px 0 11px;

      font-size: 1.75rem;
    }

    p {
      margin-bottom: 18px;

      font-size: 0.86rem;
      line-height: 1.5;
    }
  }
}

.service-tag {
  color: #98a2b3;

  font-size: 0.72rem;

  letter-spacing: 0.15em;
  text-transform: uppercase;

  @media (max-width: 767px) {
    font-size: 0.63rem;
  }
}

.service-link {
  display: inline-flex;
  align-items: center;

  gap: 8px;

  color: #102b53;

  text-decoration: none;

  font-size: 0.88rem;

  @media (max-width: 767px) {
    font-size: 0.8rem;
  }
}

/* =========================================================
   PORTFOLIO
========================================================= */

.portfolio-section {
  height: 100vh;
  min-height: 100vh;

  padding: 200px 8% 80px;

  display: flex;
  flex-direction: column;
  justify-content: center;

  box-sizing: border-box;
  overflow: hidden;

  background: #f7f8fb;

  @media (max-width: 767px) {
    height: 100svh;
    min-height: 100svh;
    max-height: 100svh;

    padding:
      105px 20px max(28px, env(safe-area-inset-bottom));

    justify-content: flex-start;
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    padding: 170px 6% 80px;
  }

  @media (min-width: 1200px) {
    padding: 200px 8% 80px;
  }
}

.portfolio-heading {
  max-width: 820px;

  margin-bottom: 45px;

  h2 {
    margin: 15px 0 0;

    font-size: clamp(3rem, 5vw, 5.4rem);
    line-height: 1.04;

    font-weight: 300;

    letter-spacing: -0.045em;

    span {
      display: block;

      color: #d9a9b5;

      font-style: italic;
    }
  }

  @media (max-width: 767px) {
    flex: 0 0 auto;

    max-width: 100%;
    margin-bottom: 20px;

    h2 {
      margin-top: 8px;

      font-size: clamp(2.05rem, 8.8vw, 2.9rem);
      line-height: 1;
    }
  }
}

.portfolio-grid {
  display: grid;
  grid-template-columns: 1.35fr 0.8fr;

  gap: 26px;

  .portfolio-item:nth-child(3) {
    grid-column: 2;
  }

  @media (max-width: 767px) {
    width: calc(100% + 20px);

    margin-right: -20px;

    flex: 1;
    min-height: 0;

    display: flex;

    gap: 12px;

    overflow-x: auto;
    overflow-y: hidden;

    padding-right: 20px;
    padding-bottom: 8px;

    scroll-snap-type: x mandatory;

    -webkit-overflow-scrolling: touch;
    scrollbar-width: none;

    &::-webkit-scrollbar {
      display: none;
    }

    .portfolio-item:nth-child(3) {
      grid-column: auto;
    }
  }
}

.portfolio-item {
  color: #102b53;

  text-decoration: none;

  &:hover {
    .portfolio-placeholder {
      transform: scale(0.985);

      span {
        transform: scale(1.1);
      }
    }

    .portfolio-arrow {
      transform: translate(4px, -4px);
    }
  }

  @media (max-width: 767px) {
    width: 78vw;
    min-width: 78vw;

    height: 100%;
    min-height: 0;

    display: flex;
    flex-direction: column;

    scroll-snap-align: start;
  }
}

.portfolio-large {
  grid-row: span 2;

  @media (max-width: 767px) {
    grid-row: auto;
  }
}

.portfolio-placeholder {
  min-height: 250px;

  display: flex;
  align-items: center;
  justify-content: center;

  background:
    linear-gradient(145deg,
      rgba(16, 43, 83, 0.9),
      rgba(45, 68, 108, 0.75));

  overflow: hidden;

  transition: transform 0.3s ease;

  span {
    color: rgba(255, 255, 255, 0.15);

    font-size: clamp(5rem, 10vw, 10rem);
    font-weight: 300;

    transition: transform 0.3s ease;
  }

  @media (max-width: 767px) {
    flex: 1;
    min-height: 0;

    border-radius: 20px;

    span {
      font-size: clamp(5rem, 24vw, 8rem);
    }
  }
}

.portfolio-placeholder-pink {
  background:
    linear-gradient(145deg,
      rgba(217, 169, 181, 0.95),
      rgba(247, 207, 213, 0.95));
}

.portfolio-placeholder-blue {
  background:
    linear-gradient(145deg,
      rgba(193, 216, 245, 0.95),
      rgba(224, 235, 249, 0.95));
}

.portfolio-info {
  padding: 20px 2px 10px;

  display: flex;
  align-items: flex-start;
  justify-content: space-between;

  p {
    margin: 0 0 5px;

    color: #98a2b3;

    font-size: 0.76rem;

    letter-spacing: 0.08em;
    text-transform: uppercase;
  }

  h3 {
    margin: 0;

    font-size: 1.45rem;
    font-weight: 400;
  }

  @media (max-width: 767px) {
    padding: 12px 2px 2px;

    p {
      font-size: 0.64rem;
    }

    h3 {
      font-size: 1.2rem;
    }
  }
}

.portfolio-arrow {
  font-size: 1.4rem;

  transition: transform 0.25s ease;
}

/* =========================================================
   CTA
========================================================= */

.cta-section {
  height: 100vh;
  min-height: 100vh;

  padding: 200px 8% 80px;

  display: grid;
  grid-template-columns: 0.7fr 1fr;

  align-items: center;

  gap: 80px;

  box-sizing: border-box;
  overflow: hidden;

  background: #ffffff;

  @media (max-width: 767px) {
    height: 100svh;
    min-height: 100svh;

    padding:
      105px 20px max(28px, env(safe-area-inset-bottom));

    grid-template-columns: 1fr;
    grid-template-rows: minmax(0, 0.85fr) auto;

    align-content: center;

    gap: 24px;
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    padding: 170px 6% 80px;

    gap: 50px;
  }

  @media (min-width: 1200px) {
    padding: 200px 8% 80px;
  }
}

.cta-logo {
  min-height: 360px;

  display: flex;
  align-items: center;
  justify-content: center;

  background: rgba(217, 169, 181, 0.09);

  border-radius:
    50% 50% 46% 54% / 46% 44% 56% 54%;

  img {
    width: 58%;
    max-height: 280px;

    display: block;

    object-fit: contain;
  }

  @media (max-width: 767px) {
    width: min(220px, 60vw);
    height: 100%;
    min-height: 0;
    max-height: 240px;

    margin: 0 auto;

    img {
      width: 60%;
      max-height: 145px;
    }
  }
}

.cta-content {
  h2 {
    margin: 16px 0 22px;

    font-size: clamp(3rem, 5vw, 5.5rem);
    line-height: 1.02;

    font-weight: 300;

    letter-spacing: -0.045em;

    span {
      display: block;

      color: #d9a9b5;

      font-style: italic;
    }
  }

  p {
    max-width: 590px;

    margin: 0 0 30px;

    color: #667085;

    line-height: 1.8;
  }

  @media (max-width: 767px) {
    h2 {
      margin: 10px 0 14px;

      font-size: clamp(2.4rem, 10vw, 3.4rem);
      line-height: 1;
    }

    p {
      margin-bottom: 18px;

      font-size: 0.86rem;
      line-height: 1.5;
    }

    .primary-btn {
      width: auto;
      min-height: 44px;

      padding: 0 20px;
    }
  }
}

/* =========================================================
   SMALL PHONES
========================================================= */

@media (max-width: 390px) {
  .hero {
    padding-top: 100px;

    gap: 14px;
  }

  .hero-content {
    h1 {
      font-size: clamp(2.3rem, 11vw, 3rem);
    }

    p {
      font-size: 0.82rem;
    }
  }

  .hero-actions {
    margin-top: 14px;

    gap: 6px;
  }

  .hero-actions .primary-btn,
  .hero-actions .secondary-btn {
    min-height: 40px;

    font-size: 0.72rem;
  }

  .art-card {
    width: min(150px, 43vw);
  }

  .intro-section,
  .services-section,
  .portfolio-section,
  .cta-section {
    padding-left: 17px;
    padding-right: 17px;
  }

  .intro-content {
    h2 {
      font-size: clamp(2.2rem, 10vw, 3rem);
    }

    p {
      font-size: 0.84rem;
    }
  }

  .section-heading {
    h2 {
      font-size: clamp(1.9rem, 8vw, 2.4rem);
    }
  }

  .portfolio-heading {
    h2 {
      font-size: clamp(1.95rem, 8.3vw, 2.5rem);
    }
  }

  .service-card,
  .portfolio-item {
    width: 82vw;
    min-width: 82vw;
  }

  .cta-content {
    h2 {
      font-size: clamp(2.2rem, 9.5vw, 3rem);
    }
  }
}
</style>
