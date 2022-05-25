<template>
  <div id="nav">
    <router-link>Accueil</router-link>
    <router-link>Créer ma carte</router-link>
  </div>
</template>

<script>
export default {
  name: "navVue",
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Amatic+SC:wght@700&display=swap");

router-link {
  font-family: "Amatic SC", cursive;
}

#nav {
  align-items: center;
  margin-left: auto;
  margin-right: auto;
  display: flex;
  justify-content: space-around;
  background: pink;
  border-radius: 10px;
  width: 60vw;
  height: 5vh;
}
</style>
