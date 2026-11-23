<template>
  <main class="home-page">
    <!-- HERO -->
    <section class="hero">
      <div class="hero-background"></div>

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
    <section class="intro-section">
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
    <section class="services-section">
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
            <span class="service-tag">
              Beauty
            </span>

            <h3>
              Beauty Artistry
            </h3>

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
            <span class="service-tag">
              Creative
            </span>

            <h3>
              Creative Direction
            </h3>

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
            <span class="service-tag">
              Visual
            </span>

            <h3>
              Editorial Concepts
            </h3>

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
    <section class="portfolio-section">
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
              <p>
                Beauty Editorial
              </p>

              <h3>
                Soft Form
              </h3>
            </div>

            <span class="portfolio-arrow">
              ↗
            </span>
          </div>
        </RouterLink>

        <RouterLink to="/portfolio" class="portfolio-item">
          <div class="portfolio-placeholder portfolio-placeholder-pink">
            <span>02</span>
          </div>

          <div class="portfolio-info">
            <div>
              <p>
                Creative Direction
              </p>

              <h3>
                Modern Muse
              </h3>
            </div>

            <span class="portfolio-arrow">
              ↗
            </span>
          </div>
        </RouterLink>

        <RouterLink to="/portfolio" class="portfolio-item">
          <div class="portfolio-placeholder portfolio-placeholder-blue">
            <span>03</span>
          </div>

          <div class="portfolio-info">
            <div>
              <p>
                Visual Styling
              </p>

              <h3>
                Quiet Luxury
              </h3>
            </div>

            <span class="portfolio-arrow">
              ↗
            </span>
          </div>
        </RouterLink>
      </div>
    </section>

    <!-- CTA -->
    <section class="cta-section">
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
  overflow-x: hidden;
  background: #fffdfd;
  color: #102b53;
}

.hero {
  min-height: calc(100vh - 90px);
  padding: 90px 7%;
  display: grid;
  grid-template-columns: minmax(0, 1fr) minmax(420px, 0.85fr);
  align-items: center;
  gap: 70px;
  position: relative;
  isolation: isolate;

  @media (max-width: 767px) {
    min-height: auto;
    padding: 80px 22px 55px;
    grid-template-columns: 1fr;
    gap: 45px;
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    padding: 80px 5%;
    grid-template-columns: 1fr 0.8fr;
    gap: 40px;
  }

  @media (min-width: 1200px) {
    padding: 90px 7%;
  }
}

.hero-background {
  position: absolute;
  inset: 0;
  z-index: -1;
  background:
    radial-gradient(circle at 80% 25%,
      rgba(193, 216, 245, 0.18),
      transparent 34%),
    radial-gradient(circle at 65% 70%,
      rgba(247, 207, 213, 0.18),
      transparent 30%),
    #fffdfd;

  clip-path: polygon(180px 0,
      100% 0,
      100% 100%,
      0 100%,
      0 180px,
      180px 180px);

  @media (max-width: 767px) {
    clip-path: polygon(100px 0,
        100% 0,
        100% 100%,
        0 100%,
        0 100px,
        100px 100px);
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    clip-path: polygon(150px 0,
        100% 0,
        100% 100%,
        0 100%,
        0 150px,
        150px 150px);
  }

  @media (min-width: 1200px) {
    clip-path: polygon(180px 0,
        100% 0,
        100% 100%,
        0 100%,
        0 180px,
        180px 180px);
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
    padding-top: 40px;

    h1 {
      margin-top: 18px;
      font-size: clamp(3rem, 15vw, 4.7rem);
    }

    p {
      font-size: 0.98rem;
      line-height: 1.7;
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
    background: currentColor;
  }
}

.hero-actions {
  margin-top: 38px;
  display: flex;
  align-items: center;
  gap: 15px;
  flex-wrap: wrap;
}

.primary-btn {
  min-height: 52px;
  padding: 0 28px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  background: #102b53;
  border: 1px solid #102b53;
  border-radius: 999px;
  color: #fff;
  text-decoration: none;
  font-size: 0.92rem;
  font-weight: 500;
  transition:
    transform 0.25s ease,
    background 0.25s ease;

  &:hover {
    transform: translateY(-2px);
    background: #1c3c6a;
  }
}

.secondary-btn {
  min-height: 52px;
  padding: 0 28px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  border: 1px solid rgba(16, 43, 83, 0.22);
  border-radius: 999px;
  color: #102b53;
  text-decoration: none;
  font-size: 0.92rem;
  font-weight: 500;
  transition:
    border-color 0.25s ease,
    background 0.25s ease;

  &:hover {
    border-color: #102b53;
    background: rgba(16, 43, 83, 0.04);
  }
}

.hero-art {
  min-height: 600px;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  z-index: 2;

  @media (max-width: 767px) {
    min-height: 430px;
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    min-height: 500px;
  }

  @media (min-width: 1200px) {
    min-height: 650px;
  }
}

.art-card {
  width: min(440px, 80%);
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
  border-radius: 48% 48% 46% 54% / 42% 42% 58% 58%;
  box-shadow: 0 35px 80px rgba(16, 43, 83, 0.08);

  img {
    width: 72%;
    height: 72%;
    object-fit: contain;
  }

  @media (max-width: 767px) {
    width: min(340px, 86%);
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    width: min(370px, 90%);
  }

  @media (min-width: 1200px) {
    width: min(460px, 82%);
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
}

.art-circle-two {
  width: 130px;
  height: 130px;
  bottom: 4%;
  left: 2%;
  border: 1px solid rgba(217, 169, 181, 0.5);
}

.floating-tag {
  padding: 11px 16px;
  position: absolute;
  z-index: 3;
  background: rgba(255, 255, 255, 0.88);
  border: 1px solid rgba(16, 43, 83, 0.08);
  border-radius: 999px;
  box-shadow: 0 14px 30px rgba(16, 43, 83, 0.08);
  color: #102b53;
  font-size: 0.78rem;
  letter-spacing: 0.08em;
  backdrop-filter: blur(12px);
}

.tag-one {
  top: 25%;
  left: 0;
}

.tag-two {
  right: -2%;
  bottom: 24%;
}

.intro-section {
  padding: 110px 7%;
  display: grid;
  grid-template-columns: 0.38fr 1fr;
  gap: 80px;
  background: #102b53;
  color: #fff;

  @media (max-width: 767px) {
    padding: 70px 22px;
    grid-template-columns: 1fr;
    gap: 35px;
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    padding: 85px 6%;
    gap: 50px;
  }

  @media (min-width: 1200px) {
    padding: 120px 8%;
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
    font-size: 0.78rem;
    letter-spacing: 0.16em;
    text-transform: uppercase;
    color: rgba(255, 255, 255, 0.6);
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
    color: #fff;
  }
}

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
}

.services-section {
  padding: 110px 7%;
  background: #fffdfd;

  @media (max-width: 767px) {
    padding: 70px 22px;
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    padding: 85px 6%;
  }

  @media (min-width: 1200px) {
    padding: 120px 8%;
  }
}

.section-heading {
  margin-bottom: 55px;
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
    margin-bottom: 35px;
    align-items: flex-start;
    flex-direction: column;
  }
}

.services-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  border-top: 1px solid rgba(16, 43, 83, 0.12);
  border-bottom: 1px solid rgba(16, 43, 83, 0.12);

  @media (max-width: 767px) {
    grid-template-columns: 1fr;
  }
}

.service-card {
  min-height: 420px;
  padding: 30px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
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
    color: #fff;

    p,
    .service-number,
    .service-tag {
      color: rgba(255, 255, 255, 0.7);
    }

    .service-link {
      color: #fff;
    }
  }

  @media (max-width: 767px) {
    min-height: 330px;
    border-right: none;
    border-bottom: 1px solid rgba(16, 43, 83, 0.12);

    &:last-child {
      border-bottom: none;
    }
  }
}

.service-card-featured {
  background: rgba(217, 169, 181, 0.12);
}

.service-number {
  color: #98a2b3;
  font-size: 0.75rem;
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
}

.service-tag {
  color: #98a2b3;
  font-size: 0.72rem;
  letter-spacing: 0.15em;
  text-transform: uppercase;
}

.service-link {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  color: #102b53;
  text-decoration: none;
  font-size: 0.88rem;
}

.portfolio-section {
  padding: 110px 7%;
  background: #f7f8fb;

  @media (max-width: 767px) {
    padding: 70px 22px;
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    padding: 85px 6%;
  }

  @media (min-width: 1200px) {
    padding: 120px 8%;
  }
}

.portfolio-heading {
  max-width: 820px;
  margin-bottom: 55px;

  h2 {
    margin: 15px 0 0;
    font-size: clamp(3rem, 5vw, 5.4rem);
    font-weight: 300;
    line-height: 1.04;
    letter-spacing: -0.045em;

    span {
      display: block;
      color: #d9a9b5;
      font-style: italic;
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
    grid-template-columns: 1fr;

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
}

.portfolio-large {
  grid-row: span 2;
}

.portfolio-placeholder {
  min-height: 300px;
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
}

.portfolio-arrow {
  font-size: 1.4rem;
  transition: transform 0.25s ease;
}

.cta-section {
  padding: 110px 7%;
  display: grid;
  grid-template-columns: 0.7fr 1fr;
  align-items: center;
  gap: 80px;
  background: #fff;

  @media (max-width: 767px) {
    padding: 70px 22px;
    grid-template-columns: 1fr;
    gap: 35px;
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    padding: 85px 6%;
    gap: 50px;
  }

  @media (min-width: 1200px) {
    padding: 120px 8%;
  }
}

.cta-logo {
  min-height: 380px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: rgba(217, 169, 181, 0.09);
  border-radius: 50% 50% 46% 54% / 46% 44% 56% 54%;

  img {
    width: 58%;
    max-height: 300px;
    object-fit: contain;
  }

  @media (max-width: 767px) {
    min-height: 300px;
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
}
</style>
