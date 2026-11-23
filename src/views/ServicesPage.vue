<template>
  <main class="services-page">
    <section class="services-section section-cutout">
      <div class="services-intro">
        <span class="eyebrow">
          Our Services
        </span>

        <h1>
          Creative services designed
          <span>with intention.</span>
        </h1>

        <p>
          Chelby Arts brings together beauty, styling and creative direction
          to create thoughtful, refined and expressive visual experiences.
        </p>
      </div>

      <div class="services-grid">
        <article class="service-card featured">
          <div class="service-top">
            <span class="service-number">01</span>
            <span class="service-category">Beauty</span>
          </div>

          <div class="service-content">
            <h2>Beauty Artistry</h2>

            <p>
              Refined beauty looks tailored to your features, personality and
              occasion, with a focus on detail and individuality.
            </p>

            <ul>
              <li>Event makeup</li>
              <li>Editorial beauty</li>
              <li>Personal beauty looks</li>
            </ul>
          </div>

          <RouterLink to="/contact" class="service-link">
            Enquire
            <span>↗</span>
          </RouterLink>
        </article>

        <article class="service-card">
          <div class="service-top">
            <span class="service-number">02</span>
            <span class="service-category">Creative</span>
          </div>

          <div class="service-content">
            <h2>Creative Direction</h2>

            <p>
              Visual concepts and creative direction developed around your
              brand, campaign, event or personal creative project.
            </p>

            <ul>
              <li>Concept development</li>
              <li>Visual direction</li>
              <li>Campaign styling</li>
            </ul>
          </div>

          <RouterLink to="/contact" class="service-link">
            Enquire
            <span>↗</span>
          </RouterLink>
        </article>

        <article class="service-card">
          <div class="service-top">
            <span class="service-number">03</span>
            <span class="service-category">Editorial</span>
          </div>

          <div class="service-content">
            <h2>Editorial Concepts</h2>

            <p>
              Concept-led creative styling and visual storytelling for shoots,
              campaigns, collaborations and artistic projects.
            </p>

            <ul>
              <li>Editorial concepts</li>
              <li>Creative styling</li>
              <li>Shoot direction</li>
            </ul>
          </div>

          <RouterLink to="/contact" class="service-link">
            Enquire
            <span>↗</span>
          </RouterLink>
        </article>

        <article class="service-card visual-card">
          <div class="service-top">
            <span class="service-number">04</span>
            <span class="service-category">Visual</span>
          </div>

          <div class="service-content">
            <h2>Visual Styling</h2>

            <p>
              Cohesive styling that brings beauty, colour, mood and creative
              detail together into a complete visual identity.
            </p>

            <ul>
              <li>Personal styling concepts</li>
              <li>Brand visual styling</li>
              <li>Creative mood development</li>
            </ul>
          </div>

          <RouterLink to="/contact" class="service-link">
            Enquire
            <span>↗</span>
          </RouterLink>
        </article>
      </div>
    </section>
  </main>
</template>

<style scoped lang="scss">
.services-page {
  width: 100%;
  height: 100vh;
  overflow: hidden;
  background: #ffffff;
  color: #102b53;

  @media (max-width: 767px) {
    height: auto;
    min-height: 100svh;
    overflow-y: auto;
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    height: 100vh;
  }

  @media (min-width: 1200px) {
    height: 100vh;
  }
}

.section-cutout {
  width: 100%;
  height: 100vh;
  min-height: 100vh;
  position: relative;

  clip-path: polygon(180px 0,
      100% 0,
      100% 100%,
      0 100%,
      0 180px,
      180px 180px);

  @media (max-width: 767px) {
    height: auto;
    min-height: 100svh;

    clip-path: polygon(90px 0,
        100% 0,
        100% 100%,
        0 100%,
        0 90px,
        90px 90px);
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

.services-section {
  box-sizing: border-box;
  height: 100vh;
  min-height: 100vh;
  padding: 165px 7% 55px;

  display: grid;
  grid-template-columns: minmax(280px, 0.72fr) minmax(0, 1.5fr);
  align-items: center;
  gap: 65px;

  overflow: hidden;

  background:
    radial-gradient(circle at 86% 20%,
      rgba(193, 216, 245, 0.22),
      transparent 30%),
    radial-gradient(circle at 35% 85%,
      rgba(247, 207, 213, 0.2),
      transparent 28%),
    #fffdfd;

  @media (max-width: 767px) {
    height: auto;
    min-height: 100svh;

    padding: 115px 22px 55px;

    grid-template-columns: 1fr;
    gap: 40px;

    overflow: visible;
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    padding: 145px 5% 45px;

    grid-template-columns: minmax(250px, 0.7fr) minmax(0, 1.4fr);
    gap: 35px;
  }

  @media (min-width: 1200px) {
    padding: 165px 7% 55px;

    grid-template-columns: minmax(300px, 0.72fr) minmax(0, 1.5fr);
    gap: 65px;
  }
}

.services-intro {
  max-width: 610px;
  min-width: 0;

  h1 {
    margin: 18px 0 24px;
    font-size: clamp(3.5rem, 5.2vw, 6.2rem);
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
    max-width: 520px;
    margin: 0;
    color: #667085;
    font-size: 1.02rem;
    line-height: 1.75;
  }

  @media (max-width: 767px) {
    max-width: 100%;

    h1 {
      margin: 14px 0 18px;
      font-size: clamp(2.7rem, 12vw, 4.2rem);
    }

    p {
      font-size: 0.94rem;
      line-height: 1.6;
    }
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    h1 {
      font-size: clamp(3.2rem, 5vw, 4.7rem);
    }

    p {
      font-size: 0.95rem;
    }
  }
}

.eyebrow {
  display: inline-flex;
  align-items: center;
  gap: 10px;
  color: #102b53;
  font-size: 0.74rem;
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
    gap: 8px;
    font-size: 0.64rem;
    letter-spacing: 0.15em;

    &::before {
      width: 22px;
    }
  }
}

.services-grid {
  min-width: 0;
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  border-top: 1px solid rgba(16, 43, 83, 0.12);
  border-left: 1px solid rgba(16, 43, 83, 0.12);

  @media (max-width: 767px) {
    grid-template-columns: 1fr;
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }

  @media (min-width: 1200px) {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }
}

.service-card {
  min-height: 315px;
  padding: 26px;

  display: flex;
  flex-direction: column;
  justify-content: space-between;
  gap: 22px;

  position: relative;

  border-right: 1px solid rgba(16, 43, 83, 0.12);
  border-bottom: 1px solid rgba(16, 43, 83, 0.12);

  background: rgba(255, 255, 255, 0.5);

  transition:
    background 0.3s ease,
    color 0.3s ease,
    transform 0.3s ease;

  &:hover {
    z-index: 2;
    background: #102b53;
    color: #ffffff;

    .service-number,
    .service-category,
    .service-content p,
    .service-content li {
      color: rgba(255, 255, 255, 0.72);
    }

    .service-content li::before {
      background: #d9a9b5;
    }

    .service-link {
      color: #ffffff;
    }
  }

  &.featured {
    background: rgba(247, 207, 213, 0.18);

    &:hover {
      background: #102b53;
    }
  }

  &.visual-card {
    background: rgba(193, 216, 245, 0.16);

    &:hover {
      background: #102b53;
    }
  }

  @media (max-width: 767px) {
    min-height: 300px;
    padding: 24px 20px;
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    min-height: 280px;
    padding: 22px;
  }

  @media (min-width: 1200px) {
    min-height: 315px;
    padding: 26px;
  }
}

.service-top {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 20px;
}

.service-number {
  color: #98a2b3;
  font-size: 0.72rem;
}

.service-category {
  color: #d9a9b5;
  font-size: 0.68rem;
  font-weight: 600;
  letter-spacing: 0.15em;
  text-transform: uppercase;
}

.service-content {
  h2 {
    margin: 0 0 14px;
    font-size: clamp(1.65rem, 2.2vw, 2.25rem);
    line-height: 1.1;
    font-weight: 400;
    letter-spacing: -0.025em;
  }

  p {
    max-width: 420px;
    margin: 0 0 18px;
    color: #667085;
    font-size: 0.9rem;
    line-height: 1.65;
  }

  ul {
    margin: 0;
    padding: 0;
    display: grid;
    gap: 7px;
    list-style: none;
  }

  li {
    display: flex;
    align-items: center;
    gap: 9px;
    color: #667085;
    font-size: 0.83rem;

    &::before {
      content: "";
      width: 5px;
      height: 5px;
      flex-shrink: 0;
      border-radius: 50%;
      background: #d9a9b5;
    }
  }

  @media (max-width: 767px) {
    h2 {
      font-size: 1.8rem;
    }

    p {
      font-size: 0.88rem;
    }
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    h2 {
      font-size: 1.65rem;
    }

    p {
      font-size: 0.84rem;
      line-height: 1.55;
    }

    li {
      font-size: 0.78rem;
    }
  }
}

.service-link {
  width: fit-content;
  display: inline-flex;
  align-items: center;
  gap: 10px;

  color: #102b53;

  text-decoration: none;
  font-size: 0.86rem;
  font-weight: 500;

  span {
    transition: transform 0.25s ease;
  }

  &:hover {
    span {
      transform: translate(4px, -4px);
    }
  }
}
</style>
