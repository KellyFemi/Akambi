<template>
  <div>
    <Header />
    <div
      style=""
      class="background-image bg-cover flex flex-col bg-[#951B0E] border-orange-600 md:flex-row p-5"
    >
      <div
        
        class="text-white flex space-x-0 md:space-x-16 items-center w-full md:w-3/6"
      >
        <div class="p-10 space-y-12">
          <div>
            <h1 class="w-full md:w-[450px] text-4xl font-bold">
              OSEZ BRISER LE SILENCE ET RÉVÉLER LA VÉRITÉ
            </h1>
          </div>
          <div>
            <h2 class="font-normal w-full md:w-[450px]">
              Bienvenue sur notre site de dénonciation, où chaque voix compte
              pour faire éclater les injustices et tenir les responsables pour
              leurs actes.
            </h2>
          </div>
          <div>
            <div class="flex space-x-5">
              <div>
                <!-- Bouton 2 pour ouvrir SignupForm -->
                <button
                  @click="openSignupForm"
                  class="rounded-lg  text-xs font-semibold text-center pt-3 pb-3 pl-2 pr-2  border-solid bg-blueee"
                >
                  Demande d'intervention
                </button>

                <!-- Le popup pour le formulaire d'inscription -->
                <SignupForm v-if="showModal" @close="closeSignupForm" />
              </div>
              <NuxtLink
                to="/Services"
                class="w-32 rounded-lg text-xs font-semibold text-center p-2 border-2 bg-transparent border-gray-100"
                >Autres services</NuxtLink
              >
            </div>
          </div>
        </div>
      </div>
      <div
        data-aos="fade-left"
        data-aos-duration="2000"
        class="flex place-content-center w-full md:w-3/6"
      >
        <div class="p-12">
          <img
            class="w-full md:w-[425px] h-auto"
            src="../assets/images/Group 422.png"
            alt=""
          />
        </div>
      </div>
    </div>

    <!-- Section 2 flex flex-col space-y-10 md:flex-row space-x-10-->
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

    <!-- Section 3 -->
    <div
      class="h-auto bg-beige pl-12 pr-12 pt-12 pb-20 md:pb-32 flex flex-col space-y-20 md:space-y-32"
    >
      <div class="flex flex-col-reverse md:flex-row md:space-x-14">
        <div class="w-full md:w-3/6">
          <div
            class="flex flex-col mt-10 md:mt-20 justify-between space-y-4 md:space-y-6"
          >
            <div>
              <h1 class="text-2xl md:text-4xl font-bold">
                ENQUETES DE MORALITE
              </h1>
            </div>
            <div>
              <p class="text-sm md:text-base">
                Notre équipe d'enquêteurs professionnels effectue des enquêtes
                approfondies sur la moralité des individus, que ce soit pour des
                raisons de pré-embauche, de partenariat commercial ou d'autres
                situations nécessitant une évaluation de l'intégrité et du
                comportement moral d'une personne. Nous fournissons des rapports
                détaillés et fiables pour vous aider à prendre des décisions
                éclairées.
              </p>
            </div>
            <div class="flex justify-center md:justify-start">
              <a
                href="/Enq_de_moralite"
                class="w-32 h-10 text-white rounded-lg text-xs font-semibold flex justify-center items-center place-content-center border-solid bg-blueee"
                >En savoir plus</a
              >
            </div>
          </div>
        </div>

        <div class="w-full md:w-3/6 h-60">
          <div class="flex justify-center items-center">
            <img
              class="h-auto md:h-full"
              src="../assets/images/mobile-smartphone-magnifier-sheet-white-paper-isolated-black-farm-wooden-table-mysterious-detective-game-concept.jpg"
              alt=""
            />
          </div>
        </div>
      </div>

      <div class="flex flex-col md:flex-row md:space-x-14">
        <div class="w-full md:w-3/6">
          <div class="flex justify-center items-center">
            <img
              class="h-auto md:h-full"
              src="../assets/images/truth-concept-arrangement-with-balance(2).jpg"
              alt=""
            />
          </div>
        </div>
        <div class="w-full md:w-3/6">
          <div
            class="flex flex-col mt-10 md:mt-20 justify-between space-y-4 md:space-y-6"
          >
            <div>
              <h1
                class="text-2xl md:text-4xl font-bold text-center md:text-right"
              >
                ENQUETES CRIMINELLES
              </h1>
            </div>
            <div>
              <p class="text-sm md:text-base">
                Nos enquêteurs expérimentés travaillent en étroite collaboration
                avec les autorités compétentes pour résoudre des affaires
                criminelles complexes. Nous utilisons des méthodes
                d'investigation approfondies et des techniques de collecte de
                preuves pour identifier les coupables, rassembler des preuves
                solides et contribuer à la poursuite de la justice.
              </p>
            </div>
            <div class="flex justify-center md:justify-end">
              <a
                href="/Enq_criminelles"
                class="w-32 h-10 text-white rounded-lg text-xs font-semibold text-center flex justify-center items-center place-content-center border-solid bg-blueee"
              >
                En savoir plus
              </a>
            </div>
          </div>
        </div>
      </div>

      <div class="flex flex-col-reverse md:flex-row md:space-x-14">
        <div class="w-full md:w-3/6">
          <div class="flex flex-col justify-between space-y-4 md:space-y-6">
            <div>
              <h1 class="text-2xl md:text-4xl font-bold">
                ENQUETES JUDICIAIRES
              </h1>
            </div>
            <div>
              <p class="text-sm md:text-base">
                Nos enquêteurs qualifiés collaborent étroitement avec les
                avocats et les professionnels du droit pour recueillir des
                preuves, effectuer des recherches approfondies et mener des
                investigations dans le cadre de procédures judiciaires. Nous
                nous engageons à soutenir le processus judiciaire en fournissant
                des informations objectives et fiables pour renforcer vos
                arguments et appuyer votre cas.
              </p>
            </div>
            <div class="flex justify-center md:justify-start">
              <a
                href="/Enq_judiciaire"
                class="w-32 h-10 text-white rounded-lg text-xs font-semibold text-center flex justify-center items-center place-content-center border-solid bg-blueee"
                >En savoir plus</a
              >
            </div>
          </div>
        </div>
        <div class="w-full md:w-3/6 h-60 pb-16">
          <div class="flex justify-center items-center">
            <img
              class="h-auto md:h-full"
              src="../assets/images/truth-concept-arrangement-crime-scene.jpg"
              alt=""
            />
          </div>
        </div>
      </div>
    </div>

    <!-- Section 4 -->
    <div
      data-aos="fade-up"
      data-aos-duration="1000"
      class="background-image flex place-content-center pt-20 pb-20 md:pt-0 md:pb-0 justify-center items-center h-[300px]"
    >
      <div
        class="flex flex-col space-y-5 place-content-center justify-center items-center p-4 md:p-0"
      >
        <div>
          <h1
            class="text-xl font-bold md:text-4xl text-white text-center md:text-left"
          >
            OSEZ BRISER LE SILENCE ET REVELER LA VERITE
          </h1>
        </div>
        <div>
          <p
            class="text-white text-xs text-center md:text-left w-full md:w-[730px] md:text-sm"
          >
            Notre application vous encourage à trouver le courage de parler et
            de vous exprimer. Que ce soit pour partager vos opinions, défendre
            une cause importante, dénoncer des injustices ou partager des
            expériences personnelles, nous vous invitons à briser le silence. En
            donnant une voix à vos idées et à vos vécus, vous contribuez à créer
            un monde où chacun est entendu, respecté et libre d'exprimer sa
            vérité. Joignez-vous à nous pour ouvrir des conversations
            significatives, promouvoir le changement et inspirer
            l'autonomisation individuelle et collective.
          </p>
        </div>
        <div class="flex justify-center md:justify-start">
          <!-- Bouton 2 pour ouvrir SignupForm -->
          <button @click="openSignupForm" class="rounded-lg text-white text-xs font-semibold text-center p-2 border-solid bg-blueee">Demande d'intervention</button>
        </div>
      </div>
    </div>

    <!-- Section 5 -->
    <div
      class="h-auto bg-white pl-12 pr-12 pt-12 pb-12 flex flex-col space-y-20 md:space-y-32"
    >
      <div class="flex flex-col-reverse md:flex-row md:space-x-14">
        <div class="w-full md:w-3/6">
          <div
            class="flex flex-col mt-10 md:mt-20 justify-between space-y-4 md:space-y-6"
          >
            <div>
              <h1 class="text-2xl md:text-4xl font-bold">
                RECHERCHE DE PERSONNES DISPARUE
              </h1>
            </div>
            <div class="z-20">
              <p class="text-sm z-20 md:text-base">
                Nous mettons tout en œuvre pour retrouver des personnes
                disparues en collaborant avec les autorités compétentes et en
                mobilisant nos ressources spécialisées. Notre équipe dévouée
                travaille avec diligence pour fournir des réponses et de
                l'espoir aux familles dans ces moments difficiles.
              </p>
            </div>
            <div class="flex justify-center md:justify-start">
              <a
                href="/Rech_pers_disp"
                class="w-32 h-10 text-white rounded-lg text-xs font-semibold flex justify-center items-center place-content-center border-solid bg-blueee"
                >En savoir plus</a
              >
            </div>
          </div>
        </div>

        <div class="w-full md:w-3/6 h-60">
          <div class="flex justify-center items-center">
            <img
              class="h-auto md:h-full"
              src="../assets/images/person-with-magnifying-glass.jpg"
              alt=""
            />
          </div>
        </div>
      </div>

      <div class="flex flex-col md:flex-row md:space-x-14">
        <div class="w-full md:w-3/6">
          <div class="flex justify-center items-center">
            <img
              class="h-auto md:h-full"
              src="../assets/images/closeup-cctv-camera-wall.jpg"
              alt=""
            />
          </div>
        </div>
        <div class="w-full md:w-3/6">
          <div
            class="flex flex-col mt-10 md:mt-20 justify-between space-y-4 md:space-y-6"
          >
            <div>
              <h1
                class="text-2xl md:text-4xl font-bold text-center md:text-right"
              >
                SURVEILLANCE
              </h1>
            </div>
            <div>
              <p class="text-sm md:text-base">
                Notre service de surveillance professionnel offre une
                surveillance discrète et efficace pour répondre à vos besoins
                spécifiques. Que ce soit pour des raisons personnelles ou
                professionnelles, notre équipe expérimentée utilise des
                techniques de pointe pour recueillir des informations précieuses
                et vous aider à prendre des décisions éclairées.
              </p>
            </div>
            <div class="flex justify-center md:justify-end">
              <a
                href="/Surveillance"
                class="w-32 h-10 text-white rounded-lg text-xs font-semibold text-center flex justify-center items-center place-content-center border-solid bg-blueee"
              >
                En savoir plus
              </a>
            </div>
          </div>
        </div>
      </div>

      <div class="flex flex-col-reverse md:flex-row md:space-x-14">
        <div class="w-full md:w-3/6">
          <div class="flex flex-col justify-between space-y-4 md:space-y-6">
            <div>
              <h1 class="text-2xl md:text-4xl font-bold">
                ENQUETES PRENUPTIALES
              </h1>
            </div>
            <div>
              <p class="text-sm md:text-base">
                Avant de prendre une décision aussi importante que le mariage,
                il est essentiel de connaître tous les faits. Notre équipe
                d'enquêteurs chevronnés mène des enquêtes pré-nuptiales
                approfondies pour vous fournir une image claire de votre futur
                conjoint(e). Nous vous aidons à prendre une décision éclairée et
                à protéger vos intérêts.
              </p>
            </div>
            <div class="flex justify-center md:justify-start">
              <a
                href="/Enq_prenuptiale"
                class="w-32 h-10 text-white rounded-lg text-xs font-semibold text-center flex justify-center items-center place-content-center border-solid bg-blueee"
                >En savoir plus</a
              >
            </div>
          </div>
        </div>
        <div class="w-full md:w-3/6 h-60 pb-16">
          <div class="flex justify-center items-center">
            <img
              class="h-auto md:h-full"
              src="../assets/images/top-view-frame-with-contract-wooden-judge-gavel.jpg"
              alt=""
            />
          </div>
        </div>
      </div>
    </div>
    <!-- Fin -->

    <!-- Section 6 Formulaire -->
    <div class="bg-white pb-16 pt-32 p-10 md:p-0 md:pb-16 md:pt-32">
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

    <Footer />
  </div>
</template>

<script>
import aosMixin from "../mixins/aos";
import Header from "../components/Header.vue";
import Footer from "../components/Footer.vue";
import SignupForm from "../components/SignupForm.vue";

export default {
  name: "IndexPage",
  components: { Header, Footer, SignupForm },
  mixins: [aosMixin],
  data() {
    return {
      showModal: false,
      name: "",
      email: "",
      message: "",
    };
  },

  methods: {
    submitForm() {
      // Logic for form submission
      console.log("Form submitted");
      console.log("Name:", this.name);
      console.log("Email:", this.email);
      console.log("Message:", this.message);
      // You can add your own form submission logic here
    },
    openSignupForm() {
      this.showModal = true;
    },
    closeSignupForm() {
      this.showModal = false;
    },
  },
};
</script>
<style>
/* Importez les classes utilitaires de Tailwind CSS */
@import "tailwindcss/base";
@import "tailwindcss/components";
@import "tailwindcss/utilities";

.background-image {
  background-image: url("../assets/images/Frame33.png");
  background-repeat: no-repeat;
  background-size: 100% 100%;
}
</style>
