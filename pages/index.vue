<template>
  <div>
    <nav>
      <img src="" alt="Descarte Consciente">
      <span>Início</span>
      <span>Pontos de coleta</span>
      <span>Informações</span>
    </nav>
    <section id="hero">
      <div id="water-mask"></div>
      <div> {{reached}} L</div>
      <div id="progress-bar">
        <div class="progress-background">
          <div class="progress-background-mask"></div>
        </div>
      </div>
      <div>{{progress}}%</div>
      <div>
        <div>Meta:</div>
        <div>{{goal}} L</div>
      </div>
      <div>
        <div>Tempo Restante</div>
        <div>{{7}} dias, {{3}} horas e {{59}} minutos</div>
      </div>
    </section>
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
            reached: 60000,
            goal: 100000,
            progress: 50,
        };
    }
}
</script>

<style>
#progress-bar {
  width: 80%;
  height: 50px;
  background:#11353F ;
  border: 2px solid #fff;
  border-radius: 15px;

  position: relative;

  margin: 0px auto;
}

.progress-background{
  position: relative;
    width: 80%;
    height: 50px;
    border-radius: 15px;
    background-color:blueviolet;
}

.progress-background-mask {
  position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 50px;
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
  background: #7eba7c;
  width:100%;
  position: relative;
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
