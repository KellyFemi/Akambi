<template>
  <div>
    <Header />
    <!-- Section 1 -->

    <div
      class="background2-image flex items-center justify-center place-content-center pt-24 h-64"
    >
      <!-- <img src="../assets/images/Rectangle198.png" alt="" /> -->
      <h1 class="h-full items-center text-3xl font-bold text-white">
        Enquêtes judiciaires
      </h1>
    </div>

    <!-- Section 2 -->

    <div class="flex flex-col md:flex-row justify-between p-14 md:p-20">
      <div
        class="flex flex-col space-y-5 w-full md:w-3/6 items-center justify-center place-content-center"
      >
        <p class="text-center w-full">
          Les enquêtes judiciaires sont menées pour recueillir des preuves et
          des informations pertinentes dans le cadre de procédures judiciaires.
          Notre équipe d'enquêteurs expérimentés est spécialisée dans la
          collecte d'informations juridiquement admissibles et dans la
          préparation de rapports complets pour une utilisation en cour.
        </p>

        <p class="text-center w-full">
          Nous travaillons en étroite collaboration avec les avocats et les
          clients pour comprendre les exigences spécifiques de chaque affaire.
        </p>

        <p class="text-center w-full">
          Notre expertise en matière d'enquêtes nous permet de trouver des
          preuves cruciales, d'interroger des témoins clés, de localiser des
          éléments de preuve et de fournir des informations essentielles pour
          soutenir le processus judiciaire.
        </p>
      </div>
      <div class="w-full md:w-2/6 flex flex-col space-y-5 pt-5 md:pt-9">
        <div class="aspect-w-16 aspect-h-9">
          <div
            class="shadow-2xl border-2 rounded-xl border-slate-100 shadow-red-300"
          >
            <form class="max-w-md mx-auto mt-4 p-6 bg-white rounded-lg">
              <div class="mb-4">
                <input
                  v-model="name"
                  class="bg-input shadow appearance-none border rounded w-full py-2 px-5 text-sm text-bleuee3 leading-tight focus:outline-none focus:shadow-outline"
                  type="text"
                  placeholder="Name*"
                />
              </div>
              <div class="mb-4">
                <input
                  v-model="email"
                  class="bg-input shadow appearance-none border rounded w-full py-2 px-5 text-sm text-bleuee3 leading-tight focus:outline-none focus:shadow-outline"
                  type="email"
                  placeholder="E-mail*"
                />
              </div>
              <div class="mb-4">
                <textarea
                  v-model="message"
                  class="shadow appearance-none border bg-input rounded w-full py-2 px-5 text-sm text-bleuee3 leading-tight focus:outline-none focus:shadow-outline"
                  rows="5"
                  placeholder="Enter Your Message Here*"
                ></textarea>
              </div>
              <div class="flex justify-end">
                <button
                  @click="submitForm"
                  class="bg-degradé1 w-32 font-normal text-xs hover:bg-blue-700 text-white py-2 px-4 rounded focus:outline-none focus:shadow-outline"
                  type="button"
                >
                  Submit
                </button>
              </div>
            </form>
          </div>
        </div>
        <div
          class="flex justify-between place-content-center items-center w-[80%] ml-6"
        >
          <div
            class="h-10 w-10 hover:text-white text-new rounded-full flex place-content-center justify-center items-center border-2 border-red-700 bg-red-700 hover:bg-blueee hover:border-blueee"
          >
            <svg
              class="svg1"
              xmlns="http://www.w3.org/2000/svg"
              stroke="currentColor"
              height="1em"
              viewBox="0 0 320 512"
            >
              <!--! Font Awesome Free 6.4.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
              <style>
                svg {
                  fill: none;
                }
              </style>
              <path
                d="M279.14 288l14.22-92.66h-88.91v-60.13c0-25.35 12.42-50.06 52.24-50.06h40.42V6.26S260.43 0 225.36 0c-73.22 0-121.08 44.38-121.08 124.72v70.62H22.89V288h81.39v224h100.17V288z"
              />
            </svg>
          </div>

          <div
            class="h-10 w-10 hover:text-white text-new rounded-full flex place-content-center justify-center items-center border-2 border-red-700 bg-red-700 hover:bg-blueee hover:border-blueee"
          >
            <svg
              class="svg1"
              xmlns="http://www.w3.org/2000/svg"
              stroke="currentColor"
              height="1em"
              viewBox="0 0 512 512"
            >
              <!--! Font Awesome Free 6.4.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
              <style>
                svg {
                  fill: none;
                }
              </style>
              <path
                d="M459.37 151.716c.325 4.548.325 9.097.325 13.645 0 138.72-105.583 298.558-298.558 298.558-59.452 0-114.68-17.219-161.137-47.106 8.447.974 16.568 1.299 25.34 1.299 49.055 0 94.213-16.568 130.274-44.832-46.132-.975-84.792-31.188-98.112-72.772 6.498.974 12.995 1.624 19.818 1.624 9.421 0 18.843-1.3 27.614-3.573-48.081-9.747-84.143-51.98-84.143-102.985v-1.299c13.969 7.797 30.214 12.67 47.431 13.319-28.264-18.843-46.781-51.005-46.781-87.391 0-19.492 5.197-37.36 14.294-52.954 51.655 63.675 129.3 105.258 216.365 109.807-1.624-7.797-2.599-15.918-2.599-24.04 0-57.828 46.782-104.934 104.934-104.934 30.213 0 57.502 12.67 76.67 33.137 23.715-4.548 46.456-13.32 66.599-25.34-7.798 24.366-24.366 44.833-46.132 57.827 21.117-2.273 41.584-8.122 60.426-16.243-14.292 20.791-32.161 39.308-52.628 54.253z"
              />
            </svg>
          </div>

          <div
            class="h-10 w-10 hover:text-white text-new rounded-full flex place-content-center justify-center items-center border-2 border-red-700 bg-red-700 hover:bg-blueee hover:border-blueee"
          >
            <svg
              class="svg1"
              xmlns="http://www.w3.org/2000/svg"
              height="1em"
              viewBox="0 0 448 512"
            >
              <!--! Font Awesome Free 6.4.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
              <style>
                svg {
                  fill: none;
                }
              </style>
              <path
                d="M100.28 448H7.4V148.9h92.88zM53.79 108.1C24.09 108.1 0 83.5 0 53.8a53.79 53.79 0 0 1 107.58 0c0 29.7-24.1 54.3-53.79 54.3zM447.9 448h-92.68V302.4c0-34.7-.7-79.2-48.29-79.2-48.29 0-55.69 37.7-55.69 76.7V448h-92.78V148.9h89.08v40.8h1.3c12.4-23.5 42.69-48.3 87.88-48.3 94 0 111.28 61.9 111.28 142.3V448z"
              />
            </svg>
          </div>

          <div
            class="h-10 w-10 hover:text-white text-new rounded-full flex place-content-center justify-center items-center border-2 border-red-700 bg-red-700 hover:bg-blueee hover:border-blueee"
          >
            <svg
              class="svg1"
              xmlns="http://www.w3.org/2000/svg"
              height="1em"
              viewBox="0 0 448 512"
            >
              <!--! Font Awesome Free 6.4.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->

              <path
                d="M380.9 97.1C339 55.1 283.2 32 223.9 32c-122.4 0-222 99.6-222 222 0 39.1 10.2 77.3 29.6 111L0 480l117.7-30.9c32.4 17.7 68.9 27 106.1 27h.1c122.3 0 224.1-99.6 224.1-222 0-59.3-25.2-115-67.1-157zm-157 341.6c-33.2 0-65.7-8.9-94-25.7l-6.7-4-69.8 18.3L72 359.2l-4.4-7c-18.5-29.4-28.2-63.3-28.2-98.2 0-101.7 82.8-184.5 184.6-184.5 49.3 0 95.6 19.2 130.4 54.1 34.8 34.9 56.2 81.2 56.1 130.5 0 101.8-84.9 184.6-186.6 184.6zm101.2-138.2c-5.5-2.8-32.8-16.2-37.9-18-5.1-1.9-8.8-2.8-12.5 2.8-3.7 5.6-14.3 18-17.6 21.8-3.2 3.7-6.5 4.2-12 1.4-32.6-16.3-54-29.1-75.5-66-5.7-9.8 5.7-9.1 16.3-30.3 1.8-3.7.9-6.9-.5-9.7-1.4-2.8-12.5-30.1-17.1-41.2-4.5-10.8-9.1-9.3-12.5-9.5-3.2-.2-6.9-.2-10.6-.2-3.7 0-9.7 1.4-14.8 6.9-5.1 5.6-19.4 19-19.4 46.3 0 27.3 19.9 53.7 22.6 57.4 2.8 3.7 39.1 59.7 94.8 83.8 35.2 15.2 49 16.5 66.6 13.9 10.7-1.6 32.8-13.4 37.4-26.4 4.6-13 4.6-24.1 3.2-26.4-1.3-2.5-5-3.9-10.5-6.6z"
              />
            </svg>
          </div>

          <div
            class="h-10 w-10 hover:text-white text-new rounded-full flex place-content-center justify-center items-center border-2 border-red-700 bg-red-700 hover:bg-blueee hover:border-blueee"
          >
            <svg
              class="svg1"
              xmlns="http://www.w3.org/2000/svg"
              height="1em"
              viewBox="0 0 512 512"
            >
              <!--! Font Awesome Free 6.4.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
              <style>
                .svg1 {
                  fill: #ffffff;
                }
              </style>
              <path
                d="M48 64C21.5 64 0 85.5 0 112c0 15.1 7.1 29.3 19.2 38.4L236.8 313.6c11.4 8.5 27 8.5 38.4 0L492.8 150.4c12.1-9.1 19.2-23.3 19.2-38.4c0-26.5-21.5-48-48-48H48zM0 176V384c0 35.3 28.7 64 64 64H448c35.3 0 64-28.7 64-64V176L294.4 339.2c-22.8 17.1-54 17.1-76.8 0L0 176z"
              />
            </svg>
          </div>
        </div>
      </div>
    </div>

    
    <!-- Section 3 -->
    <div
      class="bg-blueee flex p-6 justify-between items-center place-content-center"
    >
      <div class="h-8 w-32 flex items-center justify-center">
        <img src="../assets/images/Vector(2).png" alt="" />
      </div>

      <div
        class="space-y-10 md:space-y-0 md:flex md:justify-between md:w-[80%]"
      >
        <div
          data-aos="zoom-in"
          data-aos-duration="2000"
          class="h-auto w-auto rounded-lg p-4 bg-white flex flex-col justify-center items-center md:w-[300px]"
        >
          <div
            class="flex items-center justify-center place-content-center bg-bleuee2 rounded-full h-[40px] w-[40px] md:h-[50px] md:w-[50px]"
          >
            <img
              class="h-[24px] w-[24px] md:h-[30px] md:w-[30px]"
              src="../assets/images/icon-park-outline_surveillance-cameras-two.png"
              alt=""
            />
          </div>
          <div>
            <h1 class="text-lg md:text-xl font-bold">Formations</h1>
          </div>
          <div>
            <h2 class="text-center text-sm md:text-base">
              Notre programme de formation est conçu pour vous fournir les
              compétences nécessaires dans votre domaine d'intérêt.
            </h2>
          </div>
        </div>

        <div
          data-aos="zoom-in"
          data-aos-duration="3000"
          class="h-auto w-auto rounded-lg space-y-2 p-4 bg-white flex flex-col justify-center items-center md:w-[300px]"
        >
          <div
            class="flex items-center justify-center place-content-center bg-bleuee2 rounded-full h-[40px] w-[40px] md:h-[50px] md:w-[50px]"
          >
            <img
              class="h-[24px] w-[24px] md:h-[30px] md:w-[30px]"
              src="../assets/images/Vector.png"
              alt=""
            />
          </div>
          <div>
            <h1 class="text-lg md:text-xl font-bold">Surveillance</h1>
          </div>
          <div>
            <h2 class="text-center text-sm md:text-base">
              Que ce soit pour des raisons personnelles ou professionnelles,
              notre équipe expérimentée utilise des techniques de pointe pour
              recueillir des informations précieuses.
            </h2>
          </div>
        </div>

        <div
          data-aos="zoom-in"
          data-aos-duration="2000"
          class="h-auto w-auto rounded-lg space-y-2 p-4 bg-white flex flex-col justify-center items-center md:w-[300px]"
        >
          <div
            class="flex items-center justify-center place-content-center bg-bleuee2 rounded-full h-[40px] w-[40px] md:h-[50px] md:w-[50px]"
          >
            <img
              class="h-[24px] w-[24px] md:h-[30px] md:w-[30px]"
              src="../assets/images/medical-icon_i-health-education.png"
              alt=""
            />
          </div>
          <div>
            <h1 class="text-lg md:text-xl font-bold">Enquêtes</h1>
          </div>
          <div>
            <h2 class="text-center text-sm md:text-base">
              Nos enquêteurs expérimentés travaillent en étroite collaboration
              avec les autorités compétentes pour résoudre des affaires
              criminelles complexes.
            </h2>
          </div>
        </div>
      </div>

      <div class="h-8 w-32 flex items-center justify-center">
        <img src="../assets/images/Vector(3).png" alt="" />
      </div>
    </div>
    <!-- Section 6 Formulaire -->
    <div class="bg-white pb-16 pt-6 p-10 md:p-0 md:pb-16 md:pt-6">
      <div
        class="flex flex-col justify-center items-center place-content-center"
      >
        <div class="space-y-5 pb-4 max-w-[1000px] px-6">
          <h1 class="text-4xl font-bold text-bleuee3 text-center">
            Contactez-nous
          </h1>
          <p class="text-gris2 text-center">
            Nous serions ravis de pouvoir vous aider davantage. Veuillez remplir
            ce formulaire pour nous contacter.
          </p>
        </div>
        <div
          data-aos="fade-right"
          data-aos-duration="1000"
          class="flex flex-col md:flex-row justify-center"
        >
          <div class="w-full md:w-[400px]">
            <div
              class="shadow-2xl border-2 rounded-xl border-slate-100 shadow-cyan-300"
            >
              <form class="max-w-md mx-auto mt-4 p-6 bg-white rounded-lg">
                <div class="mb-4">
                  <input
                    v-model="name"
                    class="bg-input shadow appearance-none border rounded w-full py-2 px-5 text-sm text-bleuee3 leading-tight focus:outline-none focus:shadow-outline"
                    id="name"
                    type="text"
                    placeholder="Nom*"
                  />
                </div>
                <div class="mb-4">
                  <input
                    v-model="email"
                    class="bg-input shadow appearance-none border rounded w-full py-2 px-5 text-sm text-bleuee3 leading-tight focus:outline-none focus:shadow-outline"
                    id="email"
                    type="email"
                    placeholder="E-mail*"
                  />
                </div>
                <div class="mb-4">
                  <textarea
                    v-model="message"
                    class="shadow appearance-none border bg-input rounded w-full py-2 px-5 text-sm text-bleuee3 leading-tight focus:outline-none focus:shadow-outline"
                    id="message"
                    rows="5"
                    placeholder="Enter Your Message Here*"
                  ></textarea>
                </div>
                <div class="flex justify-end">
                  <button
                    @click="submitForm"
                    class="bg-degradé1 w-32 font-normal text-xs hover:bg-blue-700 text-white py-2 px-4 rounded focus:outline-none focus:shadow-outline"
                    type="button"
                  >
                    Submit
                  </button>
                </div>
              </form>
            </div>
          </div>
          <div
            data-aos="fade-left"
            data-aos-duration="2000"
            class="bg-gradient-to-r from-degradé1 to-degradé2 mt-6 w-full md:w-[410px] flex p-4 place-content-center items-center h-[285px]"
          >
            <p class="w-full text-white text-center text-sm">
              Le projet consiste à créer une plateforme en ligne pour permettre
              aux clients de signaler des infractions ou des incidents à la
              police. La plateforme doit permettre aux clients de soumettre
              leurs plaintes de manière facile et rapide, tout en assurant une
              enquête appropriée et une communication efficace entre le client
              et le poste de police. Le client doit également pouvoir faire des
              déclarations de perte d’enfant et des enquêtes sur les personnes.
            </p>
          </div>
        </div>
      </div>
    </div>

    <!-- <Carousel /> -->

    <Footer />
  </div>
</template>

<script>
// import AOS from 'aos'
// import 'aos/dist/aos.css'
import aosMixin from "../mixins/aos";
import Header from "../components/Header.vue";
import Footer from "../components/Footer.vue";
//   import Carousel from "../components/Carousel.vue";

export default {
  name: "Enq_judiciaire",
  mixins: [aosMixin],
  components: { Header, Footer },

  data() {
    return {
      name: "",
      email: "",
      message: "",
    };
  },
  // mounted() {
  //   AOS.init({ })
  // },

  methods: {
    submitForm() {
      // Logic for form submission
      console.log("Form submitted");
      console.log("Name:", this.name);
      console.log("Email:", this.email);
      console.log("Message:", this.message);
      // You can add your own form submission logic here
    },
  },
};
</script>
<style>
/* Importez les classes utilitaires de Tailwind CSS */
@import "tailwindcss/base";
@import "tailwindcss/components";
@import "tailwindcss/utilities";

/* Ajoutez une classe personnalisée pour votre composant */
.background2-image {
  /* Ajoutez la classe utilitaire de Tailwind CSS pour définir l'image en arrière-plan */
  background-image: url("../assets/images/Rectangle198.png");
  /* opacity: 0.9; */
  /* background-size: 100%; */
  background-repeat: no-repeat;
  background-size: cover;
  /* Autres styles personnalisés pour votre composant */
}
</style>
