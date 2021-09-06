<template>
  <div class="home">
    <nav class="purple">
      <h1 class="EasyJobs" >EasyJob</h1>
      <div class="nav-options">
        <h2>Para postulantes</h2>
        <h2>Soy empresa</h2>
        <div class="white-line"></div>
        <router-link to="/about" class="link">
          <button>Registrarse</button>
        </router-link>
        <router-link to="/about" class="link" >
          <button>Ingresar</button>
        </router-link>
      </div>
    </nav>

    <div  class="body" >
      <div class="center-body" >
        <div class="job-search">
          <div>
            <v-text-field
                label="Puesto o palabra clave"
                hide-details="auto"
                color="purple"
            ></v-text-field>
          </div>
          <div>

            <v-select :items="options" item-text="text" item-value="value" label="Lugar"
            ></v-select>
          </div>

          <div class="white-line" style="background-color:rebeccapurple" ></div>
          <div>
            <v-btn
                color="purple"
                elevation="2"
                class="white--text"
                rounded
            >Buscar</v-btn>
          </div>

        </div>
        <div class="job-options" >
          <v-img
            lazy-src="../images/principal.png"
            src="../images/principal.png"
            max-width="500"
            max-height="500"
          ></v-img>
          <div class="options-buttons">
            <h2>Filtra empleos por especialidad</h2>
            <v-btn
                x-large
                rounded
                class="btn-1 purple white--text"

            >Desarrolador movil</v-btn>
            <v-btn
                x-large
                rounded
                class="btn-2 purple white--text"
            >Ciencia de Datos</v-btn>
            <v-btn
                x-large
                rounded
                class="btn-3 purple white--text"
            >Diseño Gráfico</v-btn>
            <v-btn
                x-large
                rounded
                outlined
                class="btn-4 purple white--text"
            >UX Desing</v-btn>
            <v-btn
                x-large
                rounded
                class="btn-5 purple white--text"
            >Programación Web</v-btn>
          </div>

        </div>

      </div>

    </div>


  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  components: {

  },
  data() {
    return{
      options: ["Chimbote","Lima","Callao","Trujillo","Caraba","Nuevo Chimbote","San pedro","La plata","Santiago","Buenos aires"]
    }
  }

}
</script>

<style>
  .home{
    width: 100vw;
    height: 100vh;
  }
  nav {
    width: 100%;
    height: 10%;
    display: flex;
    background-color: #7E0B9F;
    justify-content: space-between;
    align-items: center;
  }
  nav h2{
    font-size: 108%;
  }
  nav button{
    background: white;
    width: 9pc;
    height: 2.7pc;
    border-radius:16px;
    font-weight: 700;
  }
  @font-face {
    font-family: HarlowSolidItalic;
    src: url(../fonts/HarlowSolidItalic.woff) format('woff') ;
  }
  .EasyJobs{
    color:white;
    margin-left:2%;
    font-family:HarlowSolidItalic;


  }
  .nav-options{

    width: 61%;
    height: 100%;
    color: white;
    display: flex;
    align-items: center;
    justify-content: space-evenly;
  }
  .white-line{
    width: 1px;
    background-color: white;
    height: 70%;
  }
  .link:visited{
    color: #7E0B9F;
  }
  .link:link{
    color:#7E0B9F;
  }
  .body{
    width: 100%;
    height: 90%;
    background-image: url(../images/background.png);
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .center-body{
    height: 89%;
    background: white;
    width: 91%;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .job-search{
    background: white;
    border: 1px solid purple;
    width: 53%;
    border-radius: 43px;
    height: 13%;
    align-items: center;
    margin: 60px 0px 0px 0px;
    display: flex;
    justify-content: space-evenly;
    align-content: center;

  }

  .job-options{
    background: transparent;
    width: 100%;
    height: 87%;
    display: flex;
    align-items: center;
    justify-content: space-evenly;
  }
  .v-label{
    color:purple !important;
  }
  .v-input--hide-details{
    margin-bottom: 14px !important;
  }
  .v-input--is-dirty{
    margin-top:15px !important;
  }
  .options-buttons{
    width: 44%;
    height: 80%;
    background-color:transparent;
    display: grid;
    grid-template-rows: 0.5fr 1fr 1fr;
    align-items: center;
    grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr;
  }
  .options-buttons h2{
    grid-column: 1/12;
    font-size: 2.5rem;
    color: #7e027e;
  }
  .btn-1{
    font-size: 12px !important;
    grid-row: 2;
    grid-column: 1/4;
    height: 77px !important;
    width: 186px !important;
    font-weight: bold !important;
  }
  .btn-2{
    font-size: 14px !important;
    grid-row: 2;
    grid-column: 5/8;
    height: 77px !important;
    width: 186px !important;
    font-weight: bold !important;
  }
  .btn-3{
    font-size: 14px !important;
    grid-row: 2;
    grid-column: 9/12;
    height: 77px !important;
    width: 186px !important;
    font-weight: bold !important;
  }
  .btn-4{
    grid-row: 3;
    grid-column: 3/6;
    font-size: 14px !important;
    height: 77px !important;
    width: 186px !important;
    font-weight: bold !important;
  }
  .btn-5{
    grid-row: 3;
    grid-column: 7/10;
    font-size: 12px !important;
    height: 77px !important;
    width: 186px !important;
    font-weight: bold !important;
  }

</style>
