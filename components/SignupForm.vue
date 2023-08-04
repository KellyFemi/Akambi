<template>
  <div
    class="modal fixed top-0 z-40 left-0 w-full h-full flex items-center justify-center"
  >
    <div
      class="modal-overlay absolute w-full h-full bg-gray-800 opacity-50"
    ></div>

    <div
      class="modal-container bg-white pb-2 w-[70%] md:w-[30%] mx-auto rounded shadow-lg z-50 overflow-y-auto"
    >
      <div class="modal-content py-4 space-y-5 text-left px-6">
        <div class="flex justify-between items-center pb-3">
          <p class="text-red-700 text-base md:text-lg font-semibold">
            S'inscrire
          </p>
          <button
            class="modal-close cursor-pointer z-50"
            @click="$emit('close')"
          >
            <svg
              class="fill-current text-black"
              xmlns="http://www.w3.org/2000/svg"
              width="24"
              height="24"
              viewBox="0 0 18 18"
            >
              <path
                d="M13.06 13.06l-1.06 1.06L9 10.06 5.94 13.12l-1.06-1.06L7.94 9 4.88 5.94l1.06-1.06L9 7.94l3.06-3.06 1.06 1.06L10.06 9z"
                ></path>
              </svg>
            </button>
          </div>
          

        <form @submit.prevent="submitForm" class="space-y-5">
          <input
            v-model="name"
            type="text"
            id="name"
            class="w-full rounded-lg bg-white border-2 border-gray-100 p-2 h-9 md:p-3"
            placeholder="Nom"
          />
          <input
            v-model="prenom"
            class="w-full rounded-lg bg-white border-2 border-gray-100 p-2 h-9 md:p-3"
            type="text"
            placeholder="Prénom"
          />

          <input
            v-model="email"
            type="email"
            id="email"
            class="w-full rounded-lg bg-white border-2 border-gray-100 p-2 h-9 md:p-3"
            placeholder="Email"
          />
          <input
            v-model="telephone"
            class="w-full rounded-lg bg-white border-2 border-gray-100 p-2 h-9 md:p-3"
            type="text"
            placeholder="Telephone"
          />
          <input
            v-model="password"
            type="password"
            id="password"
            class="w-full rounded-lg bg-white border-2 border-gray-100 p-2 h-9 md:p-3"
            placeholder="Mot de passe"
          />

          <div class=" text-gray-400 flex space-x-2">
            <input type="checkbox" name="" id="" >
            <h1 class=" text-xs md:text-sm">
              En créant un compte, vous acceptez nos termes et conditions et notre
              politique de confidentialité.
            </h1>
          </div>
          <div
            class="rounded-lg bg-blueee w-full md:py-3 h-8 flex place-content-center items-center"
          >
            <button type="submit" class="text-white text-center">
              S'inscrire
            </button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SignupForm",
  data() {
    return {
      name: "",
      prenom: "",
      email: "",
      password: "",
      telephone: "",
    };
  },
  methods: {
    submitForm() {
      // Ajoutez ici la logique pour envoyer les données du formulaire
      // par exemple, en utilisant une requête HTTP vers votre API d'inscription
      // et gérer la réponse
      // Ensuite, réinitialisez les champs du formulaire
      this.name = "";
      this.prenom = "";
      this.email = "";
      this.password = "";
      this.telephone = "";

      // Émettre un événement pour fermer le popup après l'inscription réussie
      this.$emit("close");
    },
  },
};
</script>
