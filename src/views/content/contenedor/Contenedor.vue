<template>
  <div>
    <div class="pref" v-if="mostrar">
      <Preferencias />
    </div>

    <div v-if="!mostrar">
      <NavBarV />
      <v-main app style="background-color: #ffffff !important">
        <router-view />
      </v-main>
    </div>
  </div>
</template>
<script>
import NavBarV from "@/components/Navbar/NavBarV.vue";
import Preferencias from "@/views/content/preferences/PreferenceCateg.vue";
import { mapState } from "vuex";

export default {
  name: "Contenedor",
  components: {
    NavBarV,
    Preferencias,
  },
  data() {
    return {
      mostrar: false,
      status_user: null,
      barraMenu: true,
    };
  },

  computed: {
    ...mapState("course", ["courseHover"]),
  },
  methods: {
    barmenu() {
      this.barraMenu = !this.barraMenu;
    },
  },
  created() {
    this.status_user = localStorage.getItem("status_preference");
    if (this.status_user == 0) {
      this.mostrar = !this.mostrar;
    }
  },
};
</script>

<style lang="scss" scoped>
.btnflo {
  height: 60px;
  width: 60px;
  position: fixed;
  bottom: 20px;
  right: 20px;
  cursor: pointer;
}
@media (max-width: 1000px) {
  .v-application--wrap {
    background-color: none !important;
    min-height: inherit;
  }
}

.view {
  overflow-y: scroll;
  background-repeat: none;
  background-size: 100% 100%;
  transition: 0.5s;
  backdrop-filter: blur(10px);
  height: 100vh;
}

.content {
  width: 100%;
  height: 100%;
  position: relative;
  display: flex;
}

.pref {
  height: 100vh;
  width: 100%;
  position: absolute;
  z-index: 9999;
  background: var(--bg-content);
}

.content-user {
  display: flex;
  width: 100%;
  max-height: 100%;
  flex-direction: column;
}
@media screen and(max-width: 1024px) {
  .sidebar-mobile {
    position: absolute;
    z-index: 32;
  }
  .sidebar-none {
    position: absolute;
    z-index: 32;
  }
  .barrita {
    visibility: visible !important;
  }
}
.barrita {
  position: absolute;
  top: 0;
  margin: 1.3rem 1rem;
  z-index: 31;
  font-size: 25px;
  visibility: hidden;
  cursor: pointer;
}
</style>
