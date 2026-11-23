<template>
  <main class="contact-page">
    <section class="contact-section section-cutout">
      <div class="contact-copy">
        <span class="eyebrow">Contact</span>

        <h1>
          Let’s create
          <span>something memorable.</span>
        </h1>

        <p class="lead">
          Tell us about your idea, event, campaign or creative project and
          we’ll get back to you with the next steps.
        </p>

        <div class="contact-details">
          <div class="contact-item">
            <span class="contact-label">Email</span>
            <a href="mailto:hello@chelbyarts.com">
              hello@chelbyarts.com
            </a>
          </div>

          <div class="contact-item">
            <span class="contact-label">Instagram</span>
            <a href="https://www.instagram.com/" target="_blank" rel="noopener noreferrer">
              @chelbyarts
            </a>
          </div>

          <div class="contact-item">
            <span class="contact-label">Location</span>
            <p>Australia</p>
          </div>
        </div>
      </div>

      <div class="contact-form-wrap">
        <div class="form-header">
          <span>Start a conversation</span>
          <p>Share a few details about what you have in mind.</p>
        </div>

        <form class="contact-form" @submit.prevent="submitForm">
          <div class="form-row">
            <div class="field">
              <label for="name">Name</label>

              <input id="name" v-model="form.name" type="text" placeholder="Your name" required />
            </div>

            <div class="field">
              <label for="email">Email</label>

              <input id="email" v-model="form.email" type="email" placeholder="you@example.com" required />
            </div>
          </div>

          <div class="field">
            <label for="service">What are you interested in?</label>

            <select id="service" v-model="form.service" required>
              <option value="" disabled>
                Select a service
              </option>

              <option value="Beauty Artistry">
                Beauty Artistry
              </option>

              <option value="Creative Direction">
                Creative Direction
              </option>

              <option value="Editorial Concepts">
                Editorial Concepts
              </option>

              <option value="Visual Styling">
                Visual Styling
              </option>

              <option value="Other">
                Other
              </option>
            </select>
          </div>

          <div class="field">
            <label for="message">
              Tell us about your project
            </label>

            <textarea id="message" v-model="form.message"
              placeholder="Tell us a little about your idea, date, location or what you would like to create."
              required></textarea>
          </div>

          <button class="submit-btn" type="submit" :disabled="loading">
            {{ loading ? "Sending..." : "Send Enquiry" }}
            <span v-if="!loading">↗</span>
          </button>

          <p v-if="successMessage" class="success-message">
            {{ successMessage }}
          </p>

          <p v-if="errorMessage" class="error-message">
            {{ errorMessage }}
          </p>
        </form>
      </div>
    </section>
  </main>
</template>

<script lang="ts">
export default {
  name: "ContactPage",

  data() {
    return {
      form: {
        name: "",
        email: "",
        service: "",
        message: "",
      },

      loading: false,
      successMessage: "",
      errorMessage: "",
    };
  },

  methods: {
    async submitForm() {
      this.loading = true;
      this.successMessage = "";
      this.errorMessage = "";

      try {
        const payload = {
          name: this.form.name,
          email: this.form.email,
          service: this.form.service,
          message: this.form.message,
        };

        console.log("Contact form:", payload);

        // Add your API call here.

        this.successMessage =
          "Thank you. Your enquiry has been received.";

        this.resetForm();
      } catch (error) {
        console.error(error);

        this.errorMessage =
          "Something went wrong. Please try again.";
      } finally {
        this.loading = false;
      }
    },

    resetForm() {
      this.form = {
        name: "",
        email: "",
        service: "",
        message: "",
      };
    },
  },
};
</script>

<style scoped lang="scss">
.contact-page {
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

.contact-section {
  width: 100%;
  height: 100vh;
  min-height: 100vh;
  box-sizing: border-box;

  padding: 170px 8% 60px;

  display: grid;
  grid-template-columns:
    minmax(0, 0.85fr) minmax(420px, 1fr);

  align-items: center;
  gap: 80px;

  overflow: hidden;

  background:
    radial-gradient(circle at 82% 20%,
      rgba(193, 216, 245, 0.24),
      transparent 30%),
    radial-gradient(circle at 28% 82%,
      rgba(247, 207, 213, 0.22),
      transparent 28%),
    #fffdfd;

  @media (max-width: 767px) {
    height: auto;
    min-height: 100svh;

    padding: 115px 22px 50px;

    grid-template-columns: 1fr;
    gap: 42px;

    overflow: visible;
  }

  @media (min-width: 768px) and (max-width: 1199px) {
    padding: 150px 5% 50px;

    grid-template-columns:
      minmax(0, 0.8fr) minmax(360px, 1fr);

    gap: 45px;
  }
}

.contact-copy {
  max-width: 690px;

  h1 {
    margin: 18px 0 24px;

    font-size: clamp(4rem, 5.8vw, 6.8rem);
    line-height: 0.96;

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
    max-width: 560px;
    margin: 0 0 34px;

    color: #667085;

    font-size: 1.04rem;
    line-height: 1.75;
  }

  @media (max-width: 767px) {
    h1 {
      font-size: clamp(2.8rem, 12vw, 4.4rem);
    }

    .lead {
      font-size: 0.94rem;
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
    background: currentColor;
  }
}

.contact-details {
  max-width: 480px;
  display: grid;
  gap: 18px;
}

.contact-item {
  padding-bottom: 16px;

  display: grid;
  grid-template-columns: 105px 1fr;

  align-items: center;
  gap: 20px;

  border-bottom: 1px solid rgba(16, 43, 83, 0.1);

  .contact-label {
    color: #98a2b3;

    font-size: 0.68rem;
    font-weight: 600;

    letter-spacing: 0.14em;
    text-transform: uppercase;
  }

  a,
  p {
    margin: 0;

    color: #102b53;

    font-size: 0.94rem;
    text-decoration: none;
  }
}

.contact-form-wrap {
  width: 100%;
  max-width: 650px;

  box-sizing: border-box;

  padding: 34px;

  justify-self: end;

  background: rgba(255, 255, 255, 0.78);

  border: 1px solid rgba(16, 43, 83, 0.08);
  border-radius: 28px;

  box-shadow:
    0 30px 80px rgba(16, 43, 83, 0.08);

  backdrop-filter: blur(16px);

  @media (max-width: 767px) {
    max-width: 100%;

    padding: 24px 20px;
    border-radius: 22px;
  }
}

.form-header {
  margin-bottom: 26px;

  >span {
    display: block;
    margin-bottom: 8px;

    color: #102b53;

    font-size: 1.65rem;
    font-weight: 400;
  }

  p {
    margin: 0;

    color: #667085;

    font-size: 0.9rem;
    line-height: 1.6;
  }
}

.contact-form {
  display: grid;
  gap: 18px;
}

.form-row {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 16px;

  @media (max-width: 767px) {
    grid-template-columns: 1fr;
  }
}

.field {
  display: grid;
  gap: 8px;

  label {
    color: #102b53;

    font-size: 0.72rem;
    font-weight: 600;
  }

  input,
  select,
  textarea {
    width: 100%;

    box-sizing: border-box;

    border: 1px solid rgba(16, 43, 83, 0.12);
    border-radius: 14px;

    background: rgba(255, 255, 255, 0.92);

    color: #102b53;

    font: inherit;
    font-size: 0.9rem;

    outline: none;

    &:focus {
      border-color: rgba(16, 43, 83, 0.45);

      box-shadow:
        0 0 0 3px rgba(193, 216, 245, 0.28);
    }
  }

  input,
  select {
    height: 48px;
    padding: 0 14px;
  }

  textarea {
    min-height: 120px;
    padding: 13px 14px;
    resize: vertical;
  }
}

.submit-btn {
  min-height: 50px;
  padding: 0 26px;

  width: fit-content;

  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 10px;

  border: 0;
  border-radius: 999px;

  background: #102b53;
  color: #ffffff;

  font: inherit;
  font-size: 0.86rem;
  font-weight: 500;

  cursor: pointer;

  &:disabled {
    opacity: 0.6;
    cursor: not-allowed;
  }
}

.success-message {
  margin: 0;

  color: #3f7d61;

  font-size: 0.83rem;
}

.error-message {
  margin: 0;

  color: #b54747;

  font-size: 0.83rem;
}
</style>
