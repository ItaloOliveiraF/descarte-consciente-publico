<template>
    <div id="header">
      <div>
        <h1 id="title" class="child1" style="color: white;" >Descarte <br> Consciente</h1>
        <p class="child2" >{{reached}}k litros de água preservada</p>
      </div>
      <div>
        <img  id="img-icon" class="child3"  src="@/assets/icon.png" alt="Descarte Consciente">
      </div>
    </div>
</template>

<script>
export default {
    name: "HeaderComponent",
    data() {
        return {
             reached: 600,
        };
    }
}
</script>

<style>
#header {
  background: #29B6D1;
  width: 100%;
  height: 300px;
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
  width: 100%;
  height: 340px;
}

</style>