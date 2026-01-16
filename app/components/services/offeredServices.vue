<template>
    <section class="offered-services">
      <div class="container">
        <div class="offered-services__header">
          <h2>My Offered Services</h2>
          <p>
            At about this time of year, some months after New Year’s resolutions have been made and kept, or made and
            neglected.
          </p>
        </div>
        <div class="offered-services__grid">
          <div class="service-card" v-for="(service, index) in services" :key="index">
            <div class="service-card__icon">
              <i :class="service.icon"></i>
            </div>
            <h3 class="service-card__title">{{ service.title }}</h3>
            <p class="service-card__description">{{ service.description }}</p>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  const services = [
    {
      icon: "fas fa-paint-brush",
      title: "Web Design",
      description:
        "It is not because things are difficult that we do not dare; it is because we do not dare that they are difficult.",
    },
    {
      icon: "fas fa-code",
      title: "Web Development",
      description:
        "If you are an entrepreneur, you know that your success cannot depend on the opinions of others. Like the wind, opinions.",
    },
    {
      icon: "fas fa-camera",
      title: "Photography",
      description:
        "Do you want to be even more successful? Learn to love learning and growth. The more effort you put into improving your skills.",
    },
    {
      icon: "fas fa-image",
      title: "Clipping Path",
      description:
        "Hypnosis quit smoking methods maintain caused quite a stir in the medical world over the last two decades. There is a lot of argument.",
    },
    {
      icon: "fas fa-mobile-alt",
      title: "Apps Interface",
      description:
        "Do you sometimes have the feeling that you’re running into the same obstacles over and over again? Many of my conflicts.",
    },
    {
      icon: "fas fa-pencil-ruler",
      title: "Graphic Design",
      description:
        "You’ve heard the expression, “Just believe it and it will come.” Well, technically, that is true, however, ‘believing’ is not just thinking that.",
    },
  ];
  </script>
  
  <style lang="scss" scoped>
  .offered-services {
    padding: 60px 20px;
    text-align: center;
    background-color: #f9f9f9;
  
    &__header {
      margin-bottom: 40px;
  
      h2 {
        font-size: 36px;
        font-weight: bold;
        color: #333;
        margin-bottom: 10px;
      }
  
      p {
        font-size: 16px;
        color: #666;
        line-height: 1.6;
      }
    }
  
    &__grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 30px;
    }
  }
  
  .service-card {
    background-color: #fff;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  
    &:hover {
      transform: translateY(-5px);
      box-shadow: 0 6px 10px rgba(0, 0, 0, 0.15);
    }
  
    &__icon {
      font-size: 40px;
      color: #6c63ff;
      margin-bottom: 15px;
    }
  
    &__title {
      font-size: 18px;
      font-weight: bold;
      color: #333;
      margin-bottom: 10px;
    }
  
    &__description {
      font-size: 14px;
      color: #666;
      line-height: 1.6;
    }
  }
  </style>