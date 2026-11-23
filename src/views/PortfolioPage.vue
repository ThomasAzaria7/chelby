<template>
  <main class="portfolio-page">
    <!-- PROJECT 1 -->
    <section class="project-section section-cutout theme-pink">
      <div class="project-copy">
        <span class="eyebrow">01 / Beauty Editorial</span>

        <h1>
          Soft Form
          <span>Beauty in subtle expression.</span>
        </h1>

        <p>
          A soft beauty concept focused on clean texture, gentle colour and a
          refined editorial finish.
        </p>

        <RouterLink to="/contact" class="project-link">
          Enquire About This Style
          <span>↗</span>
        </RouterLink>
      </div>

      <div class="project-visual">
        <div class="visual-card">
          <span class="visual-number">01</span>
          <h2>Soft Form</h2>
          <p>Beauty Editorial</p>
        </div>
      </div>
    </section>

    <!-- PROJECT 2 -->
    <section class="project-section section-cutout theme-blue">
      <div class="project-copy">
        <span class="eyebrow">02 / Creative Direction</span>

        <h1>
          Modern Muse
          <span>Clean, confident, contemporary.</span>
        </h1>

        <p>
          A modern visual direction built around structure, simplicity and
          confident creative expression.
        </p>

        <RouterLink to="/contact" class="project-link">
          Enquire About This Style
          <span>↗</span>
        </RouterLink>
      </div>

      <div class="project-visual">
        <div class="visual-card">
          <span class="visual-number">02</span>
          <h2>Modern Muse</h2>
          <p>Creative Direction</p>
        </div>
      </div>
    </section>

    <!-- PROJECT 3 -->
    <section class="project-section section-cutout theme-soft">
      <div class="project-copy">
        <span class="eyebrow">03 / Visual Styling</span>

        <h1>
          Quiet Luxury
          <span>Refined without excess.</span>
        </h1>

        <p>
          A restrained styling concept where subtle detail, soft tones and
          polished simplicity take the lead.
        </p>

        <RouterLink to="/contact" class="project-link">
          Enquire About This Style
          <span>↗</span>
        </RouterLink>
      </div>

      <div class="project-visual">
        <div class="visual-card">
          <span class="visual-number">03</span>
          <h2>Quiet Luxury</h2>
          <p>Visual Styling</p>
        </div>
      </div>
    </section>

    <!-- PROJECT 4 -->
    <section class="project-section section-cutout theme-cream">
      <div class="project-copy">
        <span class="eyebrow">04 / Beauty Artistry</span>

        <h1>
          Bare Expression
          <span>Natural detail, thoughtfully elevated.</span>
        </h1>

        <p>
          A beauty-focused concept celebrating natural features through a soft,
          polished and expressive finish.
        </p>

        <RouterLink to="/contact" class="project-link">
          Enquire About This Style
          <span>↗</span>
        </RouterLink>
      </div>

      <div class="project-visual">
        <div class="visual-card">
          <span class="visual-number">04</span>
          <h2>Bare Expression</h2>
          <p>Beauty Artistry</p>
        </div>
      </div>
    </section>

    <!-- PROJECT 5 -->
    <section class="project-section section-cutout theme-lilac">
      <div class="project-copy">
        <span class="eyebrow">05 / Editorial Concept</span>

        <h1>
          Soft Identity
          <span>Visual storytelling through mood.</span>
        </h1>

        <p>
          An editorial concept exploring identity through colour, softness and
          carefully balanced visual direction.
        </p>

        <RouterLink to="/contact" class="project-link">
          Enquire About This Style
          <span>↗</span>
        </RouterLink>
      </div>

      <div class="project-visual">
        <div class="visual-card">
          <span class="visual-number">05</span>
          <h2>Soft Identity</h2>
          <p>Editorial Concept</p>
        </div>
      </div>
    </section>

    <!-- PROJECT 6 -->
    <section class="project-section section-cutout theme-warm">
      <div class="project-copy">
        <span class="eyebrow">06 / Creative Styling</span>

        <h1>
          After Light
          <span>Warmth, depth and atmosphere.</span>
        </h1>

        <p>
          A styling concept built around warm tones, depth and a softer
          cinematic approach to visual presentation.
        </p>

        <RouterLink to="/contact" class="project-link">
          Enquire About This Style
          <span>↗</span>
        </RouterLink>
      </div>

      <div class="project-visual">
        <div class="visual-card">
          <span class="visual-number">06</span>
          <h2>After Light</h2>
          <p>Creative Styling</p>
        </div>
      </div>
    </section>
  </main>
</template>

<style scoped lang="scss">
.portfolio-page {
  width: 100%;
  height: 100vh;
  overflow-x: hidden;
  overflow-y: auto;

  color: #102b53;
  background: #ffffff;

  scroll-snap-type: y mandatory;
  scroll-behavior: smooth;
  overscroll-behavior-y: contain;

  @media (max-width: 767px) {
    height: 100svh;
    scroll-snap-type: y mandatory;
  }
}

.section-cutout {
  width: 100%;
  height: 100vh;
  min-height: 100vh;

  position: relative;

  box-sizing: border-box;

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

.project-section {
  padding: 180px 8% 65px;

  display: grid;
  grid-template-columns: minmax(0, 0.85fr) minmax(360px, 1fr);

  align-items: center;
  gap: 80px;

  overflow: hidden;

  @media (max-width: 767px) {
    padding: 110px 22px 35px;

    grid-template-columns: 1fr;
    grid-template-rows: auto minmax(0, 1fr);

    gap: 25px;
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    padding: 155px 6% 55px;

    grid-template-columns: minmax(0, 0.85fr) minmax(300px, 1fr);

    gap: 45px;
  }

  @media (min-width: 1200px) {
    padding: 180px 8% 65px;
  }
}

.project-copy {
  max-width: 720px;
  position: relative;
  z-index: 2;

  h1 {
    margin: 18px 0 26px;

    font-size: clamp(4rem, 6vw, 7rem);
    line-height: 0.95;

    font-weight: 400;
    letter-spacing: -0.055em;

    span {
      display: block;
      margin-top: 10px;

      color: rgba(16, 43, 83, 0.55);

      font-size: 0.42em;
      line-height: 1.08;

      font-style: italic;
      font-weight: 300;

      letter-spacing: -0.025em;
    }
  }

  p {
    max-width: 580px;
    margin: 0 0 30px;

    color: #667085;

    font-size: 1.03rem;
    line-height: 1.75;
  }

  @media (max-width: 767px) {
    h1 {
      margin: 12px 0 16px;

      font-size: clamp(2.8rem, 13vw, 4.5rem);

      span {
        margin-top: 7px;
        font-size: 0.36em;
      }
    }

    p {
      margin-bottom: 20px;

      font-size: 0.9rem;
      line-height: 1.55;
    }
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    h1 {
      font-size: clamp(3.5rem, 5.5vw, 5.6rem);
    }

    p {
      font-size: 0.96rem;
    }
  }
}

.eyebrow {
  display: inline-flex;
  align-items: center;
  gap: 10px;

  font-size: 0.73rem;
  font-weight: 600;

  letter-spacing: 0.18em;
  text-transform: uppercase;

  color: #102b53;

  &::before {
    content: "";

    width: 32px;
    height: 1px;

    background: currentColor;
  }

  @media (max-width: 767px) {
    gap: 8px;

    font-size: 0.62rem;
    letter-spacing: 0.14em;

    &::before {
      width: 22px;
    }
  }
}

.project-link {
  min-height: 50px;
  padding: 0 25px;

  width: fit-content;

  display: inline-flex;
  align-items: center;
  gap: 10px;

  border: 1px solid #102b53;
  border-radius: 999px;

  background: #102b53;
  color: #ffffff;

  text-decoration: none;

  font-size: 0.86rem;
  font-weight: 500;

  transition:
    transform 0.25s ease,
    background 0.25s ease;

  span {
    transition: transform 0.25s ease;
  }

  &:hover {
    transform: translateY(-2px);
    background: #1d3c69;

    span {
      transform: translate(3px, -3px);
    }
  }

  @media (max-width: 767px) {
    min-height: 44px;
    padding: 0 20px;
    font-size: 0.8rem;
  }
}

.project-visual {
  height: min(62vh, 610px);

  display: flex;
  align-items: center;
  justify-content: center;

  position: relative;

  @media (max-width: 767px) {
    height: min(40vh, 330px);
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    height: min(55vh, 500px);
  }
}

.visual-card {
  width: min(520px, 90%);
  height: 100%;

  padding: 30px;

  box-sizing: border-box;

  display: flex;
  flex-direction: column;
  justify-content: space-between;

  position: relative;

  border-radius: 32px;

  background: rgba(255, 255, 255, 0.25);

  border: 1px solid rgba(255, 255, 255, 0.48);

  box-shadow:
    0 35px 80px rgba(16, 43, 83, 0.1);

  backdrop-filter: blur(8px);

  .visual-number {
    color: rgba(16, 43, 83, 0.5);

    font-size: 0.7rem;
    letter-spacing: 0.16em;
  }

  h2 {
    margin: auto 0 8px;

    font-size: clamp(3rem, 5vw, 6rem);
    line-height: 0.9;

    font-weight: 300;
    letter-spacing: -0.055em;

    color: #102b53;
  }

  p {
    margin: 0;

    color: rgba(16, 43, 83, 0.58);

    font-size: 0.72rem;
    font-weight: 600;

    letter-spacing: 0.14em;
    text-transform: uppercase;
  }

  @media (max-width: 767px) {
    width: min(300px, 86%);

    padding: 22px;

    border-radius: 24px;

    h2 {
      font-size: clamp(2.5rem, 12vw, 4rem);
    }
  }
}

/* PROJECT THEMES */

.theme-pink {
  background:
    radial-gradient(circle at 80% 22%,
      rgba(255, 255, 255, 0.7),
      transparent 30%),
    linear-gradient(145deg,
      #f8e1e7,
      #e7b7c4);
}

.theme-blue {
  background:
    radial-gradient(circle at 78% 22%,
      rgba(255, 255, 255, 0.72),
      transparent 30%),
    linear-gradient(145deg,
      #e2eef9,
      #b7d5ec);
}

.theme-soft {
  background:
    radial-gradient(circle at 75% 20%,
      rgba(255, 255, 255, 0.72),
      transparent 30%),
    linear-gradient(145deg,
      #f6e8ec,
      #dfbcc6);
}

.theme-cream {
  background:
    radial-gradient(circle at 78% 22%,
      rgba(255, 255, 255, 0.75),
      transparent 30%),
    linear-gradient(145deg,
      #faf1e9,
      #e7d0bd);
}

.theme-lilac {
  background:
    radial-gradient(circle at 78% 20%,
      rgba(255, 255, 255, 0.72),
      transparent 30%),
    linear-gradient(145deg,
      #eee9f6,
      #cec4e3);
}

.theme-warm {
  background:
    radial-gradient(circle at 78% 22%,
      rgba(255, 255, 255, 0.72),
      transparent 30%),
    linear-gradient(145deg,
      #f5e7df,
      #dbb6a5);
}
</style>
