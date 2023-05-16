<script type="text/javascript">
  
import axios from 'axios'
let API_URL = `/api/getPersonasUxd.php`
export default {
  data() {
    return {
      persona: [],
    };
  },
  mounted() {
    axios.get(API_URL)
      .then((response) => {
        this.persona = response.data.personas;
        console.log(response.data);
      })
  },
}
</script>

<template>

<ul class="grid grid-cols-2 gap-4">
  
  <li v-for="d in persona">
  <div  style="margin: 100px 10px 10px 10px">
    <a class="text-xl info" style="margin: 10px 10px 10px 10px"><b>{{ d.nombre }}</b></a> 
    
    <br>
    <div class="textoimagen">

    <img src="https://assets.stickpng.com/images/585e4beacb11b227491c3399.png"  class="imgRedonda">

    <div class="informacion" style="margin: 10px 10px 10px 10px">
      <a class="text-xl">id-{{ d.id }}</a>
     
    <a class="text-xl info" style="margin: 10px 10px 10px 10px">Edad: {{ d.edad }}</a>
    <a class="text-xl info" style="margin: 10px 10px 10px 10px">Residencia: {{ d.residencia }}</a>
    <a class="text-xl info" style="margin: 10px 10px 10px 10px">Trabajo: {{ d.trabajo }}</a>
    </div>
    </div>
  </div>
  </li>

</ul>


</template>
<style>
   .boton{
    padding: 5px;
    border-radius:50%;
   }

  .textoimagen{
    display: inline-flex;
  }
  .info{
    display: block;
  }
  .informacion{
    float: right;
  }
  .caja{
    display: inline;
  }
  .box{
    padding: 20px;
  }
  .imgRedonda {
    width:300px;
    height:300px;
    border-radius:150px;
    border:10px solid #666;
}

  
</style>