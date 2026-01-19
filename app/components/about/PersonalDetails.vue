<template>
    <section class="aboutDetails">
      <div class="aboutDetails__inner">
        <!-- Top row -->
        <div class="aboutDetails__top">
          <!-- Left image -->
          <div class="aboutDetails__media">
            <img
              class="aboutDetails__img"
              :src="imageSrc"
              :alt="imageAlt"
              loading="lazy"
            />
          </div>
  
          <!-- Right content -->
          <div class="aboutDetails__content">
            <p class="aboutDetails__kicker">{{ kicker }}</p>
            <h2 class="aboutDetails__title">{{ title }}</h2>
  
            <p class="aboutDetails__text">
              {{ description }}
            </p>
  
            <a class="aboutDetails__btn" :href="ctaHref">
              {{ ctaText }}
            </a>
          </div>
        </div>
  
        <!-- Bottom text -->
        <div class="aboutDetails__bottom">
          <p class="aboutDetails__bottomText">
            {{ bottomText1 }}
          </p>
          <p class="aboutDetails__bottomText">
            {{ bottomText2 }}
          </p>
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  defineProps({
    imageSrc: { type: String, default: "/images/about-img.png" }, 
    imageAlt: { type: String, default: "About me photo" },
  
    kicker: { type: String, default: "ABOUT ME" },
    title: { type: String, default: "PERSONAL DETAILS" },
  
    description: {
      type: String,
      default:
        "Here, I focus on a range of items and features that we use in life without giving them a second thought, such as Coca Cola. Dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco."
    },
  
    ctaText: { type: String, default: "VIEW FULL DETAILS" },
    ctaHref: { type: String, default: "#" },
  
    bottomText1: {
      type: String,
      default:
        "It won’t be a bigger problem to find one video game lover in your neighbor. Since the introduction of Virtual Game, it has been achieving great heights so far as its popularity and technological advancement are concerned. The history of video game is as interesting as a fairy tale."
    },
    bottomText2: {
      type: String,
      default:
        "The quality of today’s video game was not at all there when video game first conceptualized and played ever. During the formative years, video games were created by using various interactive electronic devices with various display formats. The first ever video game was designed in 1947 by Thomas T. Goldsmith Jr."
    }
  })
  </script>
  
  <style lang="scss" scoped>
  $bg: #ffffff;
  $text: #111827;
  $muted: #6b7280;
  $primary: #6b7cff; 
  $primary2: #66a8ff; 
  $cardShadow: 0 8px 30px rgba(0, 0, 0, 0.06);
  
  .aboutDetails {
    background: $bg;
    padding: 64px 0;
  
    &__inner {
      width: min(1180px, calc(100% - 48px));
      margin: 0 auto;
    }
  
    &__top {
      display: grid;
      grid-template-columns: 1fr 1fr;
      align-items: center;
      gap: 72px;
    }
  
    &__media {
      display: flex;
      justify-content: center;
    }
  
    &__img {
      width: 520px;
      max-width: 100%;
      height: auto;
      display: block;
      border-radius: 6px;
      box-shadow: $cardShadow;
      background: #f3f4f6;
    }
  
    &__content {
      max-width: 520px;
    }
  
    &__kicker {
      font-size: 12px;
      letter-spacing: 0.18em;
      font-weight: 600;
      color: $text;
      margin: 0 0 14px;
    }
  
    &__title {
      font-size: 40px;
      line-height: 1.1;
      font-weight: 800;
      margin: 0 0 18px;
      color: $text;
    }
  
    &__text {
      color: $muted;
      line-height: 1.75;
      font-size: 14px;
      margin: 0 0 28px;
    }
  
    &__btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      height: 46px;
      padding: 0 26px;
      border-radius: 2px;
      text-decoration: none;
      font-weight: 700;
      font-size: 13px;
      letter-spacing: 0.04em;
      color: #fff;
      background: linear-gradient(90deg, $primary 0%, $primary2 100%);
      box-shadow: 0 10px 20px rgba(102, 168, 255, 0.28);
      transition: transform 0.15s ease, filter 0.15s ease;
  
      &:hover {
        transform: translateY(-1px);
        filter: brightness(1.02);
      }
    }
  
    &__bottom {
      margin-top: 64px;
      max-width: 900px;
      margin-left: auto;
      margin-right: auto;
      text-align: center;
    }
  
    &__bottomText {
      color: $muted;
      line-height: 1.9;
      font-size: 14px;
      margin: 0 0 18px;
    }
  }
  
  /* Responsive */
  @media (max-width: 900px) {
    .aboutDetails {
      &__top {
        grid-template-columns: 1fr;
        gap: 32px;
        text-align: center;
      }
  
      &__content {
        margin: 0 auto;
      }
    }
  }
  </style>
  