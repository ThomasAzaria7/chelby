<template>
  <div class="app">
    <header class="site-header">
      <div class="brand-column">
        <RouterLink to="/" class="brand" @click="mobileOpen = false">
          <img src="@/assets/chelbylogo.svg" alt="Chelby Arts logo" class="brand-logo" />
        </RouterLink>
      </div>

      <div class="nav-column">
        <button class="menu-toggle" type="button" :class="{ active: mobileOpen }" aria-label="Toggle navigation"
          :aria-expanded="mobileOpen" @click="mobileOpen = !mobileOpen">
          <span></span>
          <span></span>
          <span></span>
        </button>

        <nav class="navigation" :class="{ open: mobileOpen }" aria-label="Main navigation">
          <RouterLink to="/" @click="mobileOpen = false">
            Home
          </RouterLink>

          <RouterLink to="/about" @click="mobileOpen = false">
            About
          </RouterLink>

          <RouterLink to="/services" @click="mobileOpen = false">
            Services
          </RouterLink>

          <RouterLink to="/portfolio" @click="mobileOpen = false">
            Portfolio
          </RouterLink>

          <RouterLink to="/contact" class="contact-link" @click="mobileOpen = false">
            Contact
          </RouterLink>
        </nav>
      </div>
    </header>

    <main class="page-content">
      <RouterView />
    </main>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";

const mobileOpen = ref(false);
</script>

<style scoped lang="scss">
.app {
  width: 100%;
  min-height: 100vh;
}

.site-header {
  width: 100%;
  height: 78px;
  display: grid;
  grid-template-columns: 180px 1fr;
  align-items: center;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 2000;
  pointer-events: none;

  @media (max-width: 767px) {
    height: 72px;
    grid-template-columns: 90px 1fr;
    background: rgba(255, 255, 255, 0.96);
    border-bottom: 1px solid rgba(16, 43, 83, 0.06);
    backdrop-filter: blur(14px);
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    height: 74px;
    grid-template-columns: 150px 1fr;
  }

  @media (min-width: 1200px) {
    height: 78px;
    grid-template-columns: 180px 1fr;
  }
}

.brand-column {
  height: 100%;
  position: relative;
  pointer-events: auto;

  @media (max-width: 767px) {
    display: flex;
    align-items: flex-start;
    justify-content: flex-start;
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    display: block;
  }

  @media (min-width: 1200px) {
    display: block;
  }
}

.brand {
  width: 180px;
  height: 180px;
  display: flex;
  align-items: center;
  justify-content: center;
  position: absolute;
  top: 0;
  left: 0;
  text-decoration: none;
  background: #ffffff;
  z-index: 3;

  @media (max-width: 767px) {
    width: 90px;
    height: 90px;
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    width: 150px;
    height: 150px;
  }

  @media (min-width: 1200px) {
    width: 180px;
    height: 180px;
  }
}

.brand-logo {
  width: 100%;
  height: 100%;
  display: block;
  object-fit: contain;

  @media (max-width: 767px) {
    width: 88px;
    height: 88px;
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    width: 148px;
    height: 148px;
  }

  @media (min-width: 1200px) {
    width: 178px;
    height: 178px;
  }
}

.nav-column {
  height: 100%;
  padding: 0 5%;
  display: flex;
  align-items: center;
  justify-content: flex-end;
  position: relative;
  pointer-events: auto;

  @media (max-width: 767px) {
    padding: 0 18px;
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    padding: 0 30px;
  }

  @media (min-width: 1200px) {
    padding: 0 5%;
  }
}

.navigation {
  display: flex;
  align-items: center;
  justify-content: flex-end;
  gap: 34px;

  a {
    position: relative;
    color: #eeacb6;
    text-decoration: none;
    font-size: 0.95rem;
    font-weight: 500;
    letter-spacing: 0.04em;
    white-space: nowrap;
    transition:
      color 0.25s ease,
      background 0.25s ease;

    &::after {
      content: "";
      width: 0;
      height: 1px;
      position: absolute;
      left: 0;
      bottom: -7px;
      background: #102b53;
      transition: width 0.25s ease;
    }

    &:hover {
      color: #216686;

      &::after {
        width: 100%;
      }
    }

    &.router-link-exact-active:not(.contact-link) {
      color: #102b53;

      &::after {
        width: 100%;
      }
    }
  }

  .contact-link {
    padding: 11px 22px;
    border: 1px solid rgba(238, 172, 182, 0.55);
    border-radius: 999px;

    &::after {
      display: none;
    }

    &:hover,
    &.router-link-active {
      background: #102b53;
      border-color: #102b53;
      color: #ffffff;
    }
  }

  @media (max-width: 767px) {
    width: calc(100vw - 32px);
    padding: 26px;
    display: flex;
    flex-direction: column;
    align-items: stretch;
    gap: 4px;
    position: absolute;
    top: 62px;
    right: 16px;
    visibility: hidden;
    opacity: 0;
    transform: translateY(-12px);
    background: rgba(255, 255, 255, 0.98);
    border: 1px solid rgba(16, 43, 83, 0.08);
    border-radius: 20px;
    box-shadow: 0 20px 60px rgba(16, 43, 83, 0.12);
    backdrop-filter: blur(18px);
    transition:
      opacity 0.25s ease,
      transform 0.25s ease,
      visibility 0.25s ease;

    &.open {
      visibility: visible;
      opacity: 1;
      transform: translateY(0);
    }

    a {
      width: 100%;
      padding: 14px 12px;
      color: #102b53;
      font-size: 0.95rem;
      border-radius: 10px;

      &::after {
        display: none;
      }

      &:hover,
      &.router-link-exact-active {
        background: rgba(238, 172, 182, 0.12);
        color: #102b53;
      }
    }

    .contact-link {
      margin-top: 10px;
      padding: 14px 18px;
      display: flex;
      justify-content: center;
      border: none;
      background: #102b53;
      color: #ffffff;

      &:hover {
        background: #1d4e70;
        color: #ffffff;
      }
    }
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    gap: clamp(14px, 2.2vw, 24px);

    a {
      font-size: clamp(0.78rem, 1.2vw, 0.9rem);
    }

    .contact-link {
      padding: 9px 16px;
    }
  }

  @media (min-width: 1200px) {
    gap: clamp(24px, 2.5vw, 40px);

    a {
      font-size: 0.95rem;
    }
  }
}

.menu-toggle {
  width: 44px;
  height: 44px;
  padding: 0;
  display: none;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  gap: 5px;
  position: relative;
  border: 0;
  border-radius: 50%;
  background: transparent;
  cursor: pointer;

  span {
    width: 22px;
    height: 1.5px;
    display: block;
    background: #102b53;
    transform-origin: center;
    transition:
      transform 0.25s ease,
      opacity 0.2s ease;
  }

  &.active {
    span {
      &:nth-child(1) {
        transform: translateY(6.5px) rotate(45deg);
      }

      &:nth-child(2) {
        opacity: 0;
      }

      &:nth-child(3) {
        transform: translateY(-6.5px) rotate(-45deg);
      }
    }
  }

  @media (max-width: 767px) {
    display: flex;
  }
}

.page-content {
  width: 100%;
  min-height: 100vh;
}
</style>
