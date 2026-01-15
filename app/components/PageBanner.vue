<template>
    <div class="page-banner">
      <div class="page-banner__content">
        <h1>{{ pageBannerHeading }}</h1>
        <p>
          <NuxtLink to="/" class="page-banner__link">Home</NuxtLink>
          <span> → </span>
          <span>{{ pageBannerHeading }}</span>
        </p>
      </div>
    </div>
  </template>
  
  <script setup>
  defineProps({
    pageBannerHeading: {
      type: String,
      required: true,
    },
  });
  </script>
  
  <style scoped lang="scss">
  .page-banner {
    background: linear-gradient(90deg, #7f7fd5, #86a8e7, #91eae4);
    color: white;
    text-align: center;
    padding: 50px 20px;
  
    &__content {
      max-width: 800px;
      margin: 0 auto;
  
      h1 {
        font-size: 48px;
        font-weight: bold;
        margin-bottom: 10px;
      }
  
      p {
        font-size: 16px;
        color: rgba(255, 255, 255, 0.8);
  
        .page-banner__link {
          color: white;
          text-decoration: none;
          font-weight: bold;
  
          &:hover {
            text-decoration: underline;
          }
        }
  
        span {
          margin: 0 5px;
        }
      }
    }
  }
  </style>