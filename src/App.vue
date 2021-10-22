<template>
  <div id="app">
    <div class="navbar-container">
      <div class="navbar-content">
        <router-link to="/"><i class="bx-sm bx bx-home"></i></router-link>
        <router-link to="/test1"><i class="bx-sm bx bx-heart"></i></router-link>
        <router-link to="/test2"><i class="bx-sm bx bx-map"></i></router-link>
        <router-link to="/test3"
          ><i class="bx-sm bx bx-message-rounded-detail"></i
        ></router-link>
      </div>
    </div>
    <router-view />
  </div>
</template>

<style lang="less">
@import "assets/style.less";
.navbar-container {
  width: 100%;
  position: fixed;
  bottom: 0;
  z-index: 4000;
  background-color: white;
  .navbar-content {
    padding: 15px;
    display: flex;
    justify-content: space-between;
    a {
      color: rgba(95, 100, 111);
      &.router-link-exact-active {
        color: rgba(70, 209, 216);
      }
    }
  }
}
</style>
