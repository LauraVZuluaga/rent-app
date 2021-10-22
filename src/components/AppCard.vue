<template>
  <div class="card">
    <div class="card-content">
      <div class="tag-card"><i class="bx bx-map"></i>Los angeles, CA</div>
      <div class="footer-card">
        <div class="action">
          <button>
            <i class="bx bx-heart"></i>
          </button>
        </div>
        <div class="footer-card-left">
          <div class="title">
            <h3>{{ title }}</h3>
          </div>
          <div class="user">
            <div class="content-user">
              <div class="img-content">
                <img :src="imgUser" alt="" />
              </div>
              <div class="username">
                {{ username }}
              </div>
            </div>
            <div class="stars">
              <span><i class="bx bxs-star"></i></span>
              <span><i class="bx bxs-star"></i></span>
              <span><i class="bx bxs-star"></i></span>
              <small>20 reviews</small>
            </div>
          </div>
        </div>
        <div class="footer-card-right">
          <div class="price">
            <h2>$ {{ price }} usd</h2>
          </div>
          <div class="rooms">
            <div class="rooms-items">
              <i class="bx bxs-bed"></i>
              2
            </div>
            <div class="rooms-items">
              <i class="bx bxs-bed"></i>
              2
            </div>
            <div class="rooms-items">
              <i class="bx bxs-bed"></i>
              2
            </div>
          </div>
        </div>
      </div>
      <img :src="imgCard" alt="" />
    </div>
  </div>
</template>

<script>
export default {
  name: "app-card",
  props: {
    title: {
      type: String,
      default: "Not found",
    },
    username: {
      type: String,
      default: "Not found",
    },
    imgUser: {
      type: String,
      default:
        "https://img.favpng.com/21/13/5/user-profile-default-computer-icons-network-video-recorder-png-favpng-7dPZA8WRdY80Uw3bdMWkEN4fR.jpg",
    },
    imgCard: {
      type: String,
      default:
        "https://images.unsplash.com/photo-1554995207-c18c203602cb?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=870&q=80",
    },
    price: {
      type: Number,
      default: 0,
    },
  },
};
</script>

<style lang="less" scoped>
// Uso scoped cuando quiero que los estilos solo se
// apliquen al componente actual
.card {
  .card-content {
    box-shadow: 0px 5px 10px -2px rgba(74, 54, 251, 0.2);
    .tag-card {
      i {
        margin-right: 6px;
      }
    }
    .footer-card {
      .action {
        position: inherit;
        left: 79%;
        bottom: 89%;
        z-index: 100;
        button {
          box-shadow: 0px 10px 20px -2px rgba(74, 54, 251, 0.2);
          color: red;
          border: none;
          outline: none;
          border-radius: 50px;
          background-color: white;
          padding: 8px;
        }
      }
      //Para que vaya al fondo, y el texto quede sobre la imagen
      position: absolute;
      //Para alineación abajo
      bottom: 0;
      width: 100%;
      //Alineación según diseño
      display: flex;
      background-color: white;
      border-radius: 15px;
      box-sizing: border-box;
      padding: 10px;
      align-items: center;
      .footer-card-right {
        //Lo que le falta respecto a card-left
        width: 50%;
        .rooms {
          //Alinear iconos de cama
          display: flex;
          justify-content: space-around;
        }
        .rooms-items {
          color: rgba(225, 207, 241);
        }
        .price {
          margin-top: 7px;
          margin-bottom: 10px;
        }
      }
      .footer-card-left {
        margin-top: 7px;
        .title {
          margin-bottom: 10px;
          text-align: start;
          display: flex;
          margin-left: 10px;
        }
        .user {
          display: flex;
          flex-direction: column;
          .stars {
            text-align: start;
            display: flex;
            align-items: center;
            color: rgba(225, 207, 241);
            margin: 10px;
            i {
              color: rgba(69, 208, 215);
            }
          }
          .content-user {
            display: flex;
            align-items: center;
            margin-left: 10px;
          }
        }
        display: flex;
        flex-direction: column;
        width: 50%;
        .username {
          margin-left: 10px;
        }
        .img-content {
          width: 34px;
          height: 34px;
          border-radius: 50px;
          overflow: hidden;
          img {
            width: 100%;
            height: 100%;
            object-fit: cover;
          }
        }
      }
    }
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
