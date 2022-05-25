<template>
  <div class="wrapper">
    <div class="bg">
      <p>Change le fond de la carte</p>
      <button @click="changeBg">option 1</button>
      <button>option 2</button>
      <button>option 3</button>
    </div>

    <div class="police">
      <p>Change le style d'écriture</p>
      <button>option 1</button>
      <button>option 2</button>
      <button>option 3</button>
    </div>

    <div class="police-color">
      <p>Change la couleur des mots</p>
      <button>option 1</button>
      <button>option 2</button>
      <button>option 3</button>
    </div>
  </div>
</template>

<script>
export default {
  nom: "boutonSelect",

  methods: {
    changeBg: function () {
      console.log(this.bg);
    },
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Amatic+SC:wght@700&family=Pacifico&display=swap");
.wrapper {
  margin-top: -10vh;
  height: 20vh;
  display: flex;
  justify-content: space-around;
}

.bg,
.police,
.police-color {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  align-content: center;
  align-items: center;
  margin-top: 20px;
  background: rgba(255, 192, 203, 0.863);
  border-radius: 15px;
  width: 20vw;
  padding: 5px;
}
button {
  margin: 5px;
  width: 5vw;
  border-radius: 50px;
  border: rgb(158, 156, 156);
}
</style>
