<template>
  <div
    class=" modal  flex flex-col z-50 justify-center items-center place-content-center  p-5 md:p-10"
  >
    <div
      class="bg-white rounded-xl w-full xl:w-[35%] xl:h-[90%] md:w-[60%] lg:w-[40%] h-[100%] md:h- [70%] lg:h-[100%] flex flex-col justify-between sm:w-[50%]"
    >
      <div
        class="flex pl-4 pr-4 md:pl-8 md:pr-8 md:pt-5 w-full h-[100%]   items-center place-content-center justify-between"
      >
        <h1 class="text-red-700 text-base md:text-lg font-semibold">S'inscrire</h1>
        <svg
        class="close-icon w-6 h-6"
        @click="$emit('close')"
        viewBox="0 0 24 24"
      >
        <path
          fill="currentColor"
          d="M13.414 12l5.293-5.293a1 1 0 1 0-1.414-1.414L12 10.586 6.707 5.293a1 1 0 1 0-1.414 1.414L10.586 12l-5.293 5.293a1 1 0 1 0 1.414 1.414L12 13.414l5.293 5.293a1 1 0 1 0 1.414-1.414L13.414 12z"
        ></path>
      </svg>
      </div>
      <div
        class="global xl:h-[40%] md:h-[100%] flex justify-center items-center place-content-center"
      >
        <div
          class="modal-content border-gray-100 border-y-2 xl:h-[90%] h-[100%] flex justify-center items-center place-content-center"
        >
          <!-- Contenu de la fenêtre modale (pop-up) -->
          <!-- Formulaire d'inscription -->
          <form
            @submit="submitForm"
            class="flex flex-col items-center place-content-center h-[100%] w-[100%] md:h-[50%] space-y-2 md:space-y-5"
          >
            <!-- Champs du formulaire -->
            <input
              v-model="nom"
              class="w-full rounded-lg bg-white border-2 border-gray-100 p-2 h-9 md:p-3"
              type="text"
              placeholder="Nom"
            />
            <input
              v-model="prenom"
              class="w-full rounded-lg bg-white border-2 border-gray-100 p-2 h-9 md:p-3"
              type="text"
              placeholder="Prénom"
            />
            <!-- <input
              v-model="adresse"
              class="w-full rounded-lg bg-white border-2 border-gray-100 p-2 h-9 md:p-3"
              type="text"
              placeholder="Adresse"
            />
            <input
              v-model="telephone"
              class="w-full rounded-lg bg-white border-2 border-gray-100 p-2 h-9 md:p-3"
              type="text"
              placeholder="Telephone"
            /> -->
            <input
              v-model="email"
              class="w-full rounded-lg bg-white border-2 border-gray-100 p-2 h-9 md:p-3"
              type="email"
              placeholder="Email"
            />
            <input
              v-model="motdepasse"
              class="w-full rounded-lg bg-white border-2 border-gray-100 p-2 h-9 md:p-3"
              type="password"
              placeholder="Mot de passe"
            />
            <div class="rounded-lg bg-blueee w-full md:py-3 h-8 flex place-content-center items-center">
              <button
                class="text-white text-center "
                type="submit"
              >
                S'inscrire
              </button>
            </div>
          </form>
        </div>
      </div>
      <div class="pl-4 pr-4 pb-3 md:pl-8 md:pr-8 text-gray-400">
        <h1 class="text-center text-xs md:text-sm">
          En créant un compte, vous acceptez nos termes et conditions et notre
          politique de confidentialité.
        </h1>
      </div>
    </div>
  </div>
</template>

<script>
//   import axios from "axios";

export default {
  name: "Modal",
  data() {
    return {
      showModal: false,

      // nom: "",
      // prenom: "",
      // adresse: "",
      // telephone: "",
      // email: "",
      // motdepasse: "",
    };
  },
  methods: {

    closeModal() {
    // Logique pour fermer la fenêtre modale
    this.showModal = false; // Définir la valeur de la propriété showModal à false pour masquer la fenêtre modale
  },
  //   submitForm(event) {
  //     event.preventDefault(); // Empêche le rechargement de la page
      // console.log("fhj");
      // const userData = {
      //   nom: this.nom,
      //   prenom: this.prenom,
      //   adresse: this.adresse,
      //   telephone: this.telephone,
      //   email: this.email,
      //   motdepasse: this.motdepasse,
      // };

      // console.log(userData);

      // Envoyer la requête à l'API Laravel ici (utilisez Axios ou Fetch)

      // Exemple avec Axios
  //     this.$axios
  //       .post(
  //         "/participants",
  //         userData,
  //         {
  //           Accept: "application/json",
  //         }
  //       )
  //       .then((response) => {
  //         // Gérer la réponse de l'API ici
  //         const responseData = response.data;
  //         // Utilisez les données renvoyées par l'API comme vous le souhaitez
  //         console.log(responseData.response); // Affichez les données dans la console par exemple
  //       })
  //       .catch((error) => {
  //         // Gérer les erreurs de l'API ici
  //         console.log(error.response);
  //       });
  //   },
  // },
 
},
}
</script>

<style scoped>
/* Styles pour la fenêtre modale (pop-up) */
.modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(6, 4, 4, 0.5);
  align-items: center;
  justify-content: center;
  z-index: 2;
}

.global {
  height: 80%;
}

.modal-content {
  background-color: white;
  border-radius: 4px;
  /* width: 30%;
    height: 70%; */
  width: 100%;
  height: 97%;
  flex-direction: column;
  padding: 30px;
}

.close-icon {
  /* position: absolute;
    top: 10px;
    right: 10px; */
  cursor: pointer;
}

.close-icon svg {
  width: 8px;
  height: 8px;
  fill: #a90808;
}
</style>