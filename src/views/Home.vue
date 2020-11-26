<template>
  <div class="home">
    <p>{{ message }}</p>
    <v-avatar color="warning lighten-2" size="56">ML</v-avatar>
    <v-btn small color="#ff0000de" rounded @click="changeType">Change</v-btn>
    <Corentin :type="aType" />
    <Corentin />
    <Corentin />
    <Corentin />
    <Corentin />
    <Corentin />
    <Corentin />
    <Corentin />
    <Television />
    <button @click="changeVariable">Change ma variable</button>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import Corentin from "@/components/Corentin.vue";
import Television from "@/components/Television.vue";

export default {
  name: "Home",
  components: {
    Corentin,
    Television,
  },
  data: function () {
    return {
      aType: "TV",

      personns: [
        {
          firstname: "Corentin",
          lastname: "Huot",
          eMail: "corentin.huot@gmail.com",
        },
        {
          firstname: "Julien",
          lastname: "Lebatard",
          eMail: "Julien.huot@gmail.com",
        },
        {
          firstname: "rezre",
          lastname: "rezre",
          eMail: "zer.huot@gmail.com",
        },
      ],
      message: "Ma Variable",
    };
  },

  methods: {
    changeType() {
      this.personns.forEach((personn) => {
        console.log({ personn });
      });
      if (this.aType == "TV") {
        this.aType = "Radio";
      } else {
        this.aType = "TV";
      }
    },
    changeVariable() {
      this.message = "Ma Variable 2";
    },
  },
};
</script>
