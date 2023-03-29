<template>
  <main>
    <header>
      <div class="imagen">
        <img
          src="data:image/jpeg;base64,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"
        />
        <h1>Y2.mate</h1>
      </div>
      <div class="opcion">
        <p>Youtube</p>
        <p>Snaptube</p>
        <p>Lark player</p>
      </div>
    </header>
    <div class="contenido">
      <div class="texto">
        <p class="mp">Contenido de Musica y Video MP3</p>
      </div>
      <div class="input">
          <input class="escribir" type="text" placeholder="Buscar cancion o viedo" />
          <input class="escribir2" type="texto" value="Empezar ->" />
      </div>
      <div class="informacion">
        <p class="tema"> Escucha tus canciones o videos te gustaran en MP3</p>
      </div>
      <div class="auidio">
          <audio controls>
            <source src="../assets/cancion.mp4">
          </audio>
        </div>
    </div>
    <footer>
    <div class="conte">
      <p class="web">
        Este sitio web es para descargar de MP3 gratuito, que le permite convertir en videos de Youtube a MP3. Puede descragar gratis todas las canciones en MP3. Admitimos la
     descarga de todos los formatos como : ( MP3,128kpbs,320kpbs,64kpbs,9kpbs,19kpbs,64kpbs,256kpbs)ACC,MP4,MAV,3GP,WMV,FLV,MO,
    WEBM,etc.Puede convertir facilmente miles de videos de Youtube.Y siempre gratis
      </p>
    </div>
   <div class="musica">
      <div class="video">
         <video  controls src="../assets/video.mp4" ></video>
         <video  controls src="../assets/mama.mp4"></video>
         <video  controls src="../assets/musica.mp4"></video>
      </div>
    </div> 

    </footer>
  </main>
</template>
<script>
export default {
  name: "Ejercicio-uno",
};
</script>

<style scoped>

footer{
  margin: auto;

}
.conte{
  margin-top: 15px;
}
.web{
  font-size: 25px;
  width: 100%;

}
video{
  width: 85px;
  padding: 10px;
}
.auidio{
  width: 100%;

}
.input{
  margin-top: 20px;

  /* margin: auto; */
}

.escribir{
  width: 30%;
margin-left: auto;
  height: 50px;
  border:2px solid palevioletred;
  /* margin:auto; */
}
.escribir2{
  margin-right: auto;
  border:2px solid palevioletred;
  text-align: center;
  background-color: palevioletred;
}
.informacion {
  font-family: Arial;
}
.tema {
  color: blueviolet;
}
.input {
  display: flex;
  margin-left: auto;
}

header {
  background-color: antiquewhite;
  display: flex;
}
.informacion{
  margin-top: 10px;
}

.imagen {
  margin-left: 1%;
  display: flex;
}
.opcion {
  display: flex;
  width: 100%;
}
img {
  margin: auto;
  height: 40px;
}
.mp {
  font-size: 40px;
}
p {
  margin: auto;

  /* font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif; */
  color: black;
  font-size: 20px;
}
.contenido {
  margin-top: 3%;
  /* background-color: rgba(10, 36, 185, 0.356); */
  border:2px solid gray;
 margin-left:10%;
 margin-right: 10%;
}
/* * {
  border: 1PX solid red;
} */
</style>