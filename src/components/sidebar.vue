<template>
  <div>
    <div id="mySidenav" class="sidenav" :style="navBarStyle">
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
    </div>

    <button class="bav-button" @click="operateBar">
      <font-awesome-icon icon="bars" />
    </button>
  </div>
</template>

<script>
export default {
  name: "Sidebar",
  data() {
    return {
      open: false,
      navBarStyle: { width: "0" },
    };
  },
  methods: {
    operateBar() {
      this.navBarStyle.width = this.open ? "0" : "10vw";
      this.open = !this.open;
    },
  },
};
</script>

<style>
.sidenav {
  height: auto;
  position: fixed;
  z-index: 1;
  top: 0;
  left: 0;
  background-color: #435561;
  overflow-x: hidden;
  transition: 0.5s;
  padding-top: 60px;
}

.sidenav a {
  padding: 8px 8px 8px 32px;
  text-decoration: none;
  font-size: 25px;
  color: #818181;
  display: block;
  transition: 0.3s;
}

.sidenav a:hover {
  color: #f1f1f1;
}

.bav-button {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 2;
  cursor: pointer;

  background-color: transparent;
  border: none;
  color: white;
  font-size: 2rem;
}
</style>
