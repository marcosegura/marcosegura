<template>
  <img class="background" src="@/assets/background-login.webp" />
</template>
<script>
export default {
  name: "FormWelcome",
  data() {
    return {
      show: false,
      showName: false,
    };
  },
  methods: {
    fadeMe() {
      setTimeout(() => {
        this.show = !this.show;
        setTimeout(() => {
          this.showName = !this.showName;
        }, 500);
      }, 450);
    },
  },
  created() {
    this.fadeMe();
  },
};
</script>
<style lang="scss" scoped>
.welcome {
  position: relative;
  display: block;
}
.welcome img {
  object-fit: cover;
  width: 100%;
}

.welcome-text {
  font-size: 65px;
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  margin: 300px auto;
  text-align: center;
  color: white;
}
.fade-enter-active,
.fade-leave-active {
  transition: opacity 1.5s;
}

.fade-enter,
.fade-leave-to {
  opacity: 0;
}
.paragraph-welcome {
  font-size: 20px;
}
@media (max-width: 783px) {
  .welcome-text {
    font-size: 56px;
  }
}
.background {
  opacity: 0.8;
  background-position: center;
  background-size: cover;
  width: 100%;
  height: 100%;
  object-fit: cover;
  padding: 0px !important;
}
</style>
