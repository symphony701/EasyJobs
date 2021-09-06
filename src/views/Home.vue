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
            <v-overflow-btn
                dense
                editable
                color="purple"
                :items="items"
            ></v-overflow-btn>
          </div>
          <div class="white-line" style="background-color:rebeccapurple" ></div>
          <div>
            <v-btn
                color="purple"
                elevation="2"
                outlined
                rounded
            >Buscar</v-btn>
          </div>

        </div>
        <div class="job-options" >
          <v-img></v-img>
          <div></div>

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
  data: () => ({
    items: ['Trujillo', 'Chimbote', 'Lima', 'Arequipa'],
  }),

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
    margin: 8px 0px;
    display: flex;
    justify-content: space-evenly;
    align-content: center;

  }

  .job-options{
    background: red;
    width: 100%;
    height: 87%;
  }
  .v-label{
    color:purple !important;
  }


</style>
