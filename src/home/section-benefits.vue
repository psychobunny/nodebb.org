<template>
  <div class="nodebb-benefits">
    <header class="section-header">
      <h2 class="title">Why NodeBB?</h2>
    </header>

    <ul class="features-list">
      <li class="feature-block">
        <home-icon icon="mobile-responsive" />
        <h3 class="title">Mobile-first responsive</h3>
        <p
          class="text"
        >NodeBB is mobile-first, allowing for a perfect experience on every device and screen.</p>
      </li>

      <li class="feature-block">
        <home-icon icon="international" />
        <h3 class="title">Internationalization</h3>
        <p class="text">Built-in localization support with over 50 languages actively translated.</p>
      </li>

      <li class="feature-block">
        <home-icon icon="searching" />
        <h3 class="title">Search optimized</h3>
        <p
          class="text"
        >Enhance your rankings with human-readable URLs, semantic HTML with embedded microdata, and more.</p>
      </li>

      <li class="feature-block">
        <home-icon icon="sai" />
        <h3 class="title">Social authentication integration</h3>
        <p
          class="text"
        >Easy sharing of content to Facebook, Google, and Twitter, bringing more visitors to your community.</p>
      </li>

      <li class="feature-block">
        <home-icon icon="streaming" />
        <h3 class="title">Real-time streaming</h3>
        <p
          class="text"
        >Interact faster with instant notifications, streaming posts, and real-time chats.</p>
      </li>

      <li class="feature-block">
        <home-icon icon="lytics" />
        <h3 class="title">Native analytics</h3>
        <p
          class="text"
        >Your analytics dashboard has the real-time tools to show what content your users enjoy most.</p>
      </li>
    </ul>

    <div class="interstitial-cta">
      <div class="text">
        <h2 class="title">Grow your community</h2>
        <h2 class="title-sub">Drive user engagement with NodeBB.</h2>
      </div>

      <div class="buttons">
        <factor-link btn="primary" size="medim" path="/product">Learn more &rarr;</factor-link>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { factorLink, factorIcon } from "@factor/ui";

export default {
  components: {
    factorLink,
    factorIcon,
    homeIcon: () => import("../product/icon.vue")
  },
  methods: {}
};
</script>
<style lang="less">
.nodebb-benefits {
  position: relative;
  margin-top: 4rem;
  .section-header {
    font-size: 1rem;
    text-align: center;
    max-width: 900px;
    margin: 0 auto;
    margin-bottom: 50px;
    letter-spacing: -0.02em;
    .title {
      font-size: 2.5rem;
      font-weight: 700;
      line-height: 1.1;
      letter-spacing: -0.025em;

      @media (max-width: 670px) {
        font-size: 2em;
        line-height: 1.2;
      }
    }
    .text {
      margin-top: 20px;
      font-weight: 400;
      font-size: 1.4rem;
      line-height: 1.6;
    }
    @media (max-width: 767px) {
      text-align: left;
    }
  }
  .features-list {
    font-size: 1rem;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-gap: 3rem;
    list-style: none;
    @media (max-width: 767px) {
      grid-template-columns: 1fr;
    }
    .feature-block {
      position: relative;
      .title {
        font-weight: 700;
        font-size: 1.4rem;
        line-height: 1.95rem;
      }
      .text {
        font-size: 1.15rem;
        line-height: 1.7rem;
        font-weight: 400;
      }
      .icon {
        margin: 1rem 0 1.5rem;
        position: relative;
        color: #1952be;
        font-size: 2rem;
        border-radius: 0.5rem;
        overflow: visible;
        -webkit-flex: none;
        -ms-flex: none;
        flex: none;
        display: block;
        width: 3rem;
        height: 3rem;
        i {
        }
        img {
        }
      }
      h3,
      p {
        margin-bottom: 10px;
      }
      p:last-child {
        margin-bottom: 0;
      }
    }
  }
  .interstitial-cta {
    display: grid;
    grid-template-columns: 1fr auto;
    align-items: center;
    padding: 2rem 2rem;
    max-width: 700px;
    margin: 4rem auto 0rem;
    background-color: #fff;
    border-radius: 0.5rem;
    box-shadow: rgba(0, 0, 0, 0.02) 0px 8px 10px 0px,
      rgba(34, 34, 34, 0.07) 0px 0px 0px 1px inset;

    @media (max-width: 767px) {
      grid-template-columns: 1fr;
    }
    .text h2 {
      &.title {
        color: var(--color-primary);
        font-weight: 700;
        font-size: 1.3rem;
      }
      font-size: 1.15rem;
      font-weight: 400;
    }
    .buttons {
      margin: 0 0 0 20px;
      @media (max-width: 767px) {
        margin: 20px 0 0 0;
      }
    }
  }
}
</style>
