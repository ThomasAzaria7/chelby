<template>
  <div class="app">
    <header class="site-header">
      <RouterLink to="/" class="brand">
        <img src="@/assets/chelbylogo.svg" alt="Chelby Arts logo" class="brand-logo" />

        <span class="brand-name">
          Chelby Arts
        </span>
      </RouterLink>

      <nav class="navigation">
        <RouterLink to="/">
          Home
        </RouterLink>

        <RouterLink to="/about">
          About
        </RouterLink>

        <RouterLink to="/services">
          Services
        </RouterLink>

        <RouterLink to="/portfolio">
          Portfolio
        </RouterLink>

        <RouterLink to="/contact" class="contact-link">
          Contact
        </RouterLink>
      </nav>
    </header>

    <main class="page-content">
      <RouterView />
    </main>
  </div>
</template>

<style scoped lang="scss">
.app {
  min-height: 100vh;
}

.site-header {
  width: 100%;
  min-height: 90px;
  padding: 12px 5%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 30px;
  background: rgba(255, 255, 255, 0.96);
  border-bottom: 1px solid rgba(16, 43, 83, 0.08);
  position: sticky;
  top: 0;
  z-index: 1000;

  @media (max-width: 767px) {
    min-height: 72px;
    padding: 10px 20px;
    gap: 15px;
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    padding: 12px 30px;
  }

  @media (min-width: 1200px) {
    padding: 12px 6%;
  }
}

.brand {
  display: flex;
  align-items: center;
  gap: 12px;
  text-decoration: none;
  flex-shrink: 0;

  @media (max-width: 767px) {
    gap: 8px;
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    gap: 10px;
  }

  @media (min-width: 1200px) {
    gap: 14px;
  }
}

.brand-logo {
  width: 68px;
  height: 68px;
  object-fit: contain;
  display: block;

  @media (max-width: 767px) {
    width: 52px;
    height: 52px;
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    width: 60px;
    height: 60px;
  }

  @media (min-width: 1200px) {
    width: 72px;
    height: 72px;
  }
}

.brand-name {
  font-size: 1.6rem;
  font-weight: 500;
  letter-spacing: 0.04em;
  color: #102b53;
  white-space: nowrap;

  @media (max-width: 767px) {
    font-size: 1.15rem;
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    font-size: 1.4rem;
  }

  @media (min-width: 1200px) {
    font-size: 1.7rem;
  }
}

.navigation {
  display: flex;
  align-items: center;
  gap: 32px;

  a {
    position: relative;
    text-decoration: none;
    color: #333;
    font-size: 0.95rem;
    font-weight: 500;
    transition:
      color 0.25s ease,
      opacity 0.25s ease;

    &::after {
      content: "";
      position: absolute;
      left: 0;
      bottom: -7px;
      width: 0;
      height: 1px;
      background: #102b53;
      transition: width 0.25s ease;
    }

    &:hover {
      color: #102b53;

      &::after {
        width: 100%;
      }
    }

    &.router-link-active:not(.contact-link) {
      color: #102b53;

      &::after {
        width: 100%;
      }
    }
  }

  .contact-link {
    padding: 11px 22px;
    border: 1px solid #102b53;
    border-radius: 999px;
    color: #102b53;

    &::after {
      display: none;
    }

    &:hover {
      background: #102b53;
      color: #fff;
    }
  }

  @media (max-width: 767px) {
    display: none;
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    gap: 20px;

    a {
      font-size: 0.9rem;
    }

    .contact-link {
      padding: 9px 16px;
    }
  }

  @media (min-width: 1200px) {
    gap: 34px;
  }
}

.page-content {
  width: 100%;
}
</style>
