<template>
    <div>
      <select v-model="selectedLanguage" @change="changeLanguage" class="px-2 py-1 rounded bg-white border-black border w-32">
        <option v-for="language in languages" :value="language.code" :key="language.code">
          <img :src="getFlagImagePath(language.flag)" :alt="language.name" class="flag-icon">
          {{ language.name }}
        </option>
      </select>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        selectedLanguage: 'fr',
        languages: [
          { code: 'fr', name: 'Français', flag: 'fr.png' },
          { code: 'en', name: 'English', flag: 'gb.png' },
          { code: 'es', name: 'Español', flag: 'es.png' },
          // Ajoutez d'autres langues selon vos besoins
        ]
      }
    },
    methods: {
      changeLanguage() {
        this.$router.push({ path: '/', query: { lang: this.selectedLanguage } });
      },
    //   getFlagImagePath(flag) {
    //     return require(`~/static/flags/${flag}`);
    //   }
      getFlagImagePath(flag) {
      return require('~/static/flags/' + flag);
    }
    },
  }
  </script>
  
  <style scoped>
  .flag-icon {
    width: 20px; /* Ajustez la taille du drapeau selon vos besoins */
    height: 20px;
    margin-right: 5px; /* Ajoutez une marge pour séparer le drapeau du texte */
  }
  </style>
  