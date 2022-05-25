<template>
  <div class="wrapper">
    <div :class="this.bg">
      <p>
        Salut c'est <span>{{ this.surname }}</span>
      </p>

      <p>je t'invite à mon anniversaire qui aura lieux le:</p>
      <p>{{ this.date }}</p>
      <p>A l'adresse suivante :</p>
      <br />
      <p>{{ this.adresse }}</p>
      <p>
        tu peux me joindre au <span>{{ this.phone }}</span>
      </p>
    </div>

    <div class="input">
      <input
        type="text"
        name="Prenom"
        id=""
        placeholder="Prenom"
        @input="changePrenom"
      />
      <input type="text" name="Date" placeholder="Date" @input="changeDate" />
      <input
        type="text"
        name="adresse"
        id=""
        placeholder="adresse"
        @input="changeAdresse"
      />
      <input
        type="number"
        name="phone"
        placeholder="phone"
        @input="changePhone"
      />
    </div>

    <div class="button-bg"></div>
    <div class="button-police"></div>
    <div class="button-color"></div>
  </div>

  <boutonSelect />
</template>

<script>
import boutonSelect from "./boutonSelect.vue";

export default {
  name: "cardDisplay",

  data() {
    return {
      surname: "",
      date: "",
      adresse: "",
      phone: "",

      bg: "cardDisplay1",
    };
  },
  component: {
    boutonSelect,
  },

  methods: {
    changePrenom: function (event) {
      this.surname = event.target.value;
    },
    changeDate: function (event) {
      this.date = event.target.value;
    },
    changeAdresse: function (event) {
      this.adresse = event.target.value;
    },
    changePhone: function (event) {
      this.phone = event.target.value;
    },

    chanfeBg: function () {
      this.bg = "cardDisplay2";
    },
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Amatic+SC:wght@700&family=Pacifico&display=swap");
.wrapper {
  height: 100vh;
  display: flex;
  align-content: space-around;
  justify-content: space-around;

  justify-content: center;
  align-items: center;
}

.cardDisplay1 {
  height: 80vh;
  width: 40vw;
  border-radius: 25px;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  align-content: center;
  font-family: "Pacifico", cursive;
  letter-spacing: 5px;
  font-size: 1.5em;
  color: black;
  background: url(../assets/redFlowers\ .png) no-repeat center/cover;
}
.cardDisplay2 {
  height: 80vh;
  width: 40vw;
  border-radius: 25px;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  align-content: center;
  font-family: "Pacifico", cursive;
  letter-spacing: 5px;
  font-size: 1.5em;
  color: black;
  background: url(../assets/pirate.png) no-repeat center/cover;
}

.input {
  margin-left: 10vh;

  display: flex;
  flex-direction: column;
  align-content: space-around;
  align-items: center;
}
input {
  margin: 1vh;
  width: 30vw;
  height: 5vh;
  border-radius: 5px;
  border: none;
  padding: 5px;
  font-family: "Amatic SC", cursive;
  letter-spacing: 5px;
  font-size: 1.5em;
  color: grey;
}
</style>
