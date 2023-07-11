<template>
    <div class="bg-blueee h-80 flex space-x-10 items-center place-content-center pl-10 pr-10">
      <div class="carousel flex-nowrap overflow-x-hidden">
        <div class="slides-container flex  space-x-10 items-center place-content-center pl-10 pr-10">
          <div
            v-for="(slide, index) in slides"
            :key="index"
            :class="['slide', { active: isActiveSlide(index) }]"
          >
            <!-- Contenu de chaque diapositive -->
            <div
              
              class="h-auto w-auto slide active rounded-lg space-y-2 p-4 bg-white flex flex-col justify-center items-center"
            >
              <div
                class="flex items-center justify-center place-content-center bg-bleuee2 rounded-full h-[50px] w-[50px]"
              >
                <img
                  class="h-[30px] w-[30px]"
                  src="../assets/images/icon-park-outline_surveillance-cameras-two.png"
                  alt=""
                />
              </div>
              <div>
                <h1 class="text-xl font-bold">{{ slide.title }}</h1>
              </div>
              <div>
                <h2 class="text-center text-base">{{ slide.description }}</h2>
              </div>
            </div>
          </div>
        </div>
  
        <div class="controls">
          <button @click="prevSlide" class="prev-button">Précédent</button>
          <button @click="nextSlide" class="next-button">Suivant</button>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        currentIndex: 0,
        slides: [
          {
            title: "Formations",
            description:
              "Notre programme de formation est conçu pour vous fournir les compétences nécessaires dans votre domaine d'intérêt.",
          },
          {
            title: "Surveillance",
            description:
              "Que ce soit pour des raisons personnelles ou professionnelles, notre équipe expérimentée utilise des techniques de pointe pour recueillir des informations précieuses.",
          },
          {
            title: "Enquêtes",
            description:
              "Nos enquêteurs expérimentés travaillent en étroite collaboration avec les autorités compétentes pour résoudre des affaires criminelles complexes.",
          },
          {
            title: "Formations",
            description:
              "Notre programme de formation est conçu pour vous fournir les compétences nécessaires dans votre domaine d'intérêt.",
          },
        ],
      };
    },
    methods: {
      isActiveSlide(index) {
        if (this.currentIndex === index) {
          return true;
        }
        if (this.currentIndex === 0 && index === this.slides.length - 1) {
          return true;
        }
        if (this.currentIndex === this.slides.length - 1 && index === 0) {
          return true;
        }
        return false;
      },
      prevSlide() {
        this.currentIndex =
          (this.currentIndex - 1 + this.slides.length) % this.slides.length;
      },
      nextSlide() {
        this.currentIndex = (this.currentIndex + 1) % this.slides.length;
      },
    },
  };
  </script>
  

<style>
.carousel {
  display: flex;
  align-items: center;
  overflow: hidden;
}

.slides-container {
  width: 100%;
  overflow: hidden;
  position: relative;
}

.slide {
  width: 100%;
  opacity: 0;
  transform: translateX(-100%);
  transition: opacity 0.3s ease, transform 0.3s ease;
}

.slide.active {
  opacity: 1;
  transform: translateX(0);
}

.controls {
  margin-top: 1rem;
}

.prev-button,
.next-button {
  background-color: #f2f2f2;
  border: none;
  padding: 0.5rem 1rem;
  cursor: pointer;
}
</style>
