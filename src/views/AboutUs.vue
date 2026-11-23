<template>
  <main class="about-page">
    <section class="about-section section-cutout">
      <div class="about-copy">
        <span class="eyebrow">
          About Chelby Arts
        </span>

        <h1>
          Creativity shaped by
          <span>beauty, identity and intention.</span>
        </h1>

        <p class="lead">
          Chelby Arts is a creative beauty studio focused on thoughtful visual
          expression, refined artistry and concepts that feel personal,
          memorable and distinct.
        </p>

        <div class="about-text">
          <p>
            Our approach goes beyond creating a finished look. We consider
            mood, detail, composition, identity and the feeling behind the final
            result.
          </p>

          <p>
            Whether working on beauty artistry, visual styling or creative
            direction, our goal is to create something that feels considered,
            expressive and true to the person or idea behind it.
          </p>
        </div>

        <RouterLink to="/contact" class="primary-btn">
          Get In Touch
        </RouterLink>
      </div>

      <div class="about-visual">
        <div class="logo-frame">
          <img src="@/assets/chelbylogo.svg" alt="Chelby Arts logo" />
        </div>

        <div class="floating-label label-one">
          Beauty
        </div>

        <div class="floating-label label-two">
          Creativity
        </div>

        <div class="floating-label label-three">
          Expression
        </div>
      </div>
    </section>
  </main>
</template>


<style scoped lang="scss">
.about-page {
  width: 100%;
  height: 100vh;
  overflow: hidden;
  background: #ffffff;
  color: #102b53;

  @media (max-width: 767px) {
    height: 100svh;
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

.about-section {
  width: 100%;
  height: 100vh;
  min-height: 100vh;
  box-sizing: border-box;
  padding: 180px 8% 60px;

  display: grid;
  grid-template-columns: minmax(0, 1fr) minmax(360px, 0.75fr);
  align-items: center;
  gap: 70px;

  overflow: hidden;

  background:
    radial-gradient(circle at 82% 25%,
      rgba(193, 216, 245, 0.24),
      transparent 32%),
    radial-gradient(circle at 68% 75%,
      rgba(247, 207, 213, 0.22),
      transparent 30%),
    #fffdfd;

  @media (max-width: 767px) {
    height: 100svh;
    min-height: 100svh;

    padding: 105px 22px 30px;

    grid-template-columns: 1fr;
    grid-template-rows: auto minmax(0, 1fr);
    align-content: center;
    align-items: center;
    gap: 24px;

    overflow-y: auto;
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    height: 100vh;
    min-height: 100vh;

    padding: 150px 6% 50px;

    grid-template-columns: minmax(0, 1fr) minmax(280px, 0.75fr);
    gap: 40px;
  }

  @media (min-width: 1200px) {
    height: 100vh;
    min-height: 100vh;

    padding: 180px 8% 60px;

    grid-template-columns: minmax(0, 1fr) minmax(360px, 0.75fr);
    gap: 70px;
  }
}

.about-copy {
  width: 100%;
  max-width: 720px;
  min-width: 0;
  position: relative;
  z-index: 2;

  h1 {
    margin: 18px 0 22px;
    font-size: clamp(3.6rem, 5.6vw, 6.5rem);
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

  .lead {
    max-width: 620px;
    margin: 0 0 20px;
    color: #3f4b5e;
    font-size: 1.05rem;
    line-height: 1.7;
  }

  @media (max-width: 767px) {
    max-width: 100%;

    h1 {
      margin: 14px 0 16px;
      font-size: clamp(2.5rem, 11vw, 3.8rem);
      line-height: 1;
    }

    .lead {
      max-width: 100%;
      margin-bottom: 14px;
      font-size: 0.92rem;
      line-height: 1.55;
    }
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    h1 {
      margin: 16px 0 20px;
      font-size: clamp(3.4rem, 5.8vw, 5rem);
    }

    .lead {
      font-size: 1rem;
      line-height: 1.65;
    }
  }

  @media (min-width: 1200px) {
    h1 {
      font-size: clamp(4rem, 5.6vw, 6.5rem);
    }
  }
}

.about-text {
  max-width: 620px;
  display: grid;
  gap: 12px;
  margin-bottom: 24px;

  p {
    margin: 0;
    color: #667085;
    font-size: 0.95rem;
    line-height: 1.65;
  }

  @media (max-width: 767px) {
    max-width: 100%;
    gap: 8px;
    margin-bottom: 18px;

    p {
      font-size: 0.86rem;
      line-height: 1.5;
    }
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    gap: 10px;
    margin-bottom: 20px;

    p {
      font-size: 0.9rem;
      line-height: 1.6;
    }
  }

  @media (min-width: 1200px) {
    gap: 12px;
    margin-bottom: 24px;
  }
}

.eyebrow {
  display: inline-flex;
  align-items: center;
  gap: 10px;
  color: #102b53;
  font-size: 0.76rem;
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
    letter-spacing: 0.14em;

    &::before {
      width: 22px;
    }
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    font-size: 0.7rem;
    letter-spacing: 0.17em;

    &::before {
      width: 28px;
    }
  }

  @media (min-width: 1200px) {
    font-size: 0.76rem;
  }
}

.primary-btn {
  min-height: 50px;
  padding: 0 27px;

  display: inline-flex;
  align-items: center;
  justify-content: center;

  border: 1px solid #102b53;
  border-radius: 999px;

  background: #102b53;
  color: #ffffff;

  text-decoration: none;
  font-size: 0.9rem;
  font-weight: 500;

  transition:
    transform 0.25s ease,
    background 0.25s ease,
    border-color 0.25s ease;

  &:hover {
    transform: translateY(-2px);
    background: #1c3c6a;
    border-color: #1c3c6a;
  }

  @media (max-width: 767px) {
    min-height: 44px;
    padding: 0 22px;
    font-size: 0.84rem;
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    min-height: 48px;
    padding: 0 24px;
    font-size: 0.87rem;
  }

  @media (min-width: 1200px) {
    min-height: 50px;
    padding: 0 27px;
  }
}

.about-visual {
  width: 100%;
  height: min(58vh, 520px);
  min-height: 0;

  display: flex;
  align-items: center;
  justify-content: center;

  position: relative;
  z-index: 1;

  @media (max-width: 767px) {
    height: min(28vh, 240px);
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    height: min(48vh, 420px);
  }

  @media (min-width: 1200px) {
    height: min(58vh, 520px);
  }
}

.logo-frame {
  width: min(430px, 90%);
  height: 100%;
  max-height: 500px;

  display: flex;
  align-items: center;
  justify-content: center;

  background:
    linear-gradient(150deg,
      rgba(217, 169, 181, 0.16),
      rgba(193, 216, 245, 0.25));

  border-radius: 50% 45% 52% 48% / 45% 48% 52% 55%;

  box-shadow:
    0 40px 90px rgba(16, 43, 83, 0.08);

  img {
    width: 67%;
    height: 67%;
    display: block;
    object-fit: contain;
  }

  @media (max-width: 767px) {
    width: min(260px, 76%);
    height: min(230px, 100%);

    img {
      width: 64%;
      height: 64%;
    }
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    width: min(340px, 88%);
    max-height: 400px;
  }

  @media (min-width: 1200px) {
    width: min(430px, 90%);
    max-height: 500px;
  }
}

.floating-label {
  padding: 9px 15px;

  position: absolute;

  background: rgba(255, 255, 255, 0.92);

  border: 1px solid rgba(16, 43, 83, 0.08);
  border-radius: 999px;

  box-shadow:
    0 14px 40px rgba(16, 43, 83, 0.08);

  color: #102b53;

  font-size: 0.73rem;
  letter-spacing: 0.08em;

  white-space: nowrap;

  backdrop-filter: blur(12px);

  @media (max-width: 767px) {
    padding: 7px 11px;
    font-size: 0.62rem;
    letter-spacing: 0.06em;
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    padding: 8px 13px;
    font-size: 0.68rem;
  }

  @media (min-width: 1200px) {
    padding: 9px 15px;
    font-size: 0.73rem;
  }
}

.label-one {
  top: 18%;
  left: 0;

  @media (max-width: 767px) {
    top: 16%;
    left: 2%;
  }
}

.label-two {
  top: 45%;
  right: -2%;

  @media (max-width: 767px) {
    top: 42%;
    right: 2%;
  }
}

.label-three {
  bottom: 12%;
  left: 10%;

  @media (max-width: 767px) {
    bottom: 10%;
    left: 7%;
  }
}
</style>
