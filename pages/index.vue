<template>
  <div>
    <div id="header">
      <div>
        <h1 id="title" class="child1" style="color: white;" >Descarte <br> Consciente</h1>
        <p class="child2" >{{reached}}k litros de água preservada</p>
      </div>
      <img  id="img-icon" class="child3"  src="@/assets/icon.png" alt="Descarte Consciente">
    </div>
    <section id="hero">
      <div id="progress"> {{progress}}%</div>
      <div id="water-mask"></div>
      <div id="progress-bar">
        <div class="progress-background">
          <div class="progress-background-mask"></div>
        </div>
      </div>
    </section>

    <div id="meta">
      <div>
        <div id="meta-litros">Meta: {{goal}} litros</div>
      </div>
      <div id="time">
        <div>Tempo Restante</div>
        <div>{{7}} dias <br> {{3}} horas <br> {{59}} minutos</div>
      </div>
    </div>

    <section id="collection-points">
      <MapsCentroConvivencia></MapsCentroConvivencia>
    </section>
    <section id="infos">
      <div>
        Por que descartar corretamente?
      </div>
      <div>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam aliquet eleifend tortor, vitae eleifend nisi facilisis a. Pellentesque quis lacus blandit, fringilla turpis a, aliquet augue. Quisque venenatis a odio quis varius. Suspendisse dictum tempus quam tincidunt molestie. Etiam sodales pellentesque hendrerit. Suspendisse porttitor velit purus. Integer elementum sapien maximus diam lacinia viverra. Duis vel mauris sed erat dictum maximus. Maecenas suscipit, lacus sagittis ultricies luctus, ipsum neque finibus nulla, ut molestie ligula ex nec dolor. Donec sit amet diam est. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.
      </div>

      <div>
        O que pode ser descartado?
      </div>
      <div>
        <div>
          Medicamentos líquidos
        </div>
        <div>
          Medicamentos sólidos
        </div>
        <div>
          Medicamentos semi sólidos
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
    name: "IndexPage",
    data() {
        return {
            reached: 600,
            goal: 100000,
            progress: 70
        };
    }
}
</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@200&display=swap');

#progress-bar {
  width: 80%;
  height: 40px;
  background:#9b9b9b ;
  border: 2px solid #fff;
  border-radius: 15px;
  left: 0px;
  position: relative  ;
  margin: 0px auto;
}

.progress-background{
  position: relative;
    width: 70%;
    height: 40px;
    border-radius: 15px;
    background-color:#29B6D1;
}

.progress-background-mask {
  position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 40px;
    border-radius: 15px;
    background-image: url('@/assets/water-mask.jpg');
    background-position: 0px;
    background-repeat: repeat-x;
    background-size: cover;

    animation: filling 10s ease-in-out infinite;
    opacity: 0.2;
}

@keyframes filling {
  0% {background-position: 100px ;}
  100% {background-position: 1000px ;}
}

#hero {
  background: white;
  width:100%;
  height: 100px;
  position: relative;
  color: #29B6D1;
  font-family: 'Roboto', sans-serif;
}

#progress {
  position: relative;
  margin-left: 150px;
  margin-top: 10px;
}

#header {
  background: #29B6D1;
  width: 100%;
  height: 330px;
  display: flex;
  justify-content: space-around;
  font-family: 'Roboto', sans-serif;
  color: white;
}

.child1 {
  height: 60%;
  width: 100%;
  justify-content: center;
  align-content: center;
  font-family: 'Roboto', sans-serif;
  font-size: 80px;
  font-weight: 900px;
  margin-top: 50px;
}


.child2 {
  height: 10%;
  width: 100%;
  margin-left: 10px;
}

.child3 {
  padding-right: 30px;
}

* {
  margin: 0px;
  padding: 0px;
}

#img-icon{
  width: 300px;
  height: 370px;
}



#meta {
  background: #29B6D1;
  width: 40%;
  height: 180px;
  color: white;
  font-family: 'Roboto', sans-serif;
  position: relative;
  left: 30%;
  border-radius: 10px;
  padding: 10px 10px 10px 10px;
}

#meta-litros {
  position: relative;
  left: 25%;
  font-size: 30px;
}

#time {
  border: 1px solid white;
  position: absolute ;
  width: 200px;
  height: 120px;
  left: 0;
  right: 0;
  top: 30px;
  bottom: 0;
  margin: auto;
  padding: 5px 5px 5px 5px;
  border-radius: 10px;
}
/* #water-mask {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: url('@/assets/water-mask.jpg');
  background-size: cover;
  background-position: 0px 2000px;
  z-index: 0;
  opacity: 0.2;
} */
</style>
