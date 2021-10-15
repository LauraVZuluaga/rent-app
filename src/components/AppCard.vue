<template>
  <div class="card">
    <div class="card-content">
      <span class="tag-card">Los Angeles CA</span>
      <img
        src="https://images.unsplash.com/photo-1554995207-c18c203602cb?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=870&q=80"
        alt=""
      />
    </div>
  </div>
</template>

<script>
export default {
  name: "app-card",
};
</script>

<style lang="less" scoped>
// Uso scoped cuando quiero que los estilos solo se
// apliquen al componente actual
.card {
  .card-content {
    border-radius: 30px;
    overflow: hidden;
    width: 100%;
    height: 300px;
    position: relative;
    .tag-card {
      position: absolute;
      background-color: rgb(244, 242, 243);
      padding: 8px;
      z-index: 2;
      top: 0;
      margin: 20px;
      border-radius: 15px;
      font-size: 0.9rem;
    }
    img {
      //Para que la imagen no se estire, uso object-fit
      //Con el cover, la imagen se acopla al espacio
      object-fit: cover;
      width: 100%;
      height: 100%;
    }
  }
}
</style>
