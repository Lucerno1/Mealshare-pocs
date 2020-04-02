<template>

  <ul id="mealList">

    <!--Dit is een loop die zich herhaalt voor alle item in items en heeft een unieke key gebaseerd op de index -->
    <li v-for="(item,index) in items" :key="'meal'+index" class="mealItem" :style="{ backgroundImage: 'url(' + item.image + ')' }">
      <div class="mealHeader"> 
        <div>{{ item.mealName }}</div>
        <div>€ {{ item.mealPrice }}</div>
      </div>
      
      <div>
       
      </div>
      {{ item.distance }} 
      {{ item.timeSpan }}
    </li>
  </ul>
  
</template>

<script>
export default {
name: "Meals",
data(){
  return{
    items: [
      { mealName: "Stamppot", mealPrice: 3, distance: 0.5, timeSpan: "18:00 - 18:30", image:"https://lh3.googleusercontent.com/proxy/0TCxfHF_K2aW3Jraum6__w6i5v5QnvOSofytVM7TjM-xBM-qWaZ15h3vXlmPAdV4WxLKTH0mr48W3c8IC4ld4duVz3IKfaBWSrVlKE9EULm2FtRf1grKuA" },
      { mealName: "Spaghetti Bolognese", mealPrice: 3, distance: 0.5, timeSpan: "18:00 - 18:30", image:"https://i.pinimg.com/originals/94/c1/e4/94c1e4010bbda1e790db61d8c3d75e36.png" },
      { mealName: "Spinazie Quiche", mealPrice: 4, distance: 0.5, timeSpan: "18:00 - 18:30", image:"https://healthinut.com/wp-content/uploads/2018/01/Quiche-met-spinazie-en-geitenkaas-2.jpg" },
    ],
  }
}

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  background-color:grey;
  height:25vh;
  margin:20px;
  max-width:100vw; 
}
a {
  color: #42b983;
}

#mealList {
  max-width:100vw;
}

.mealHeader {
  display:flex;
  justify-content:space-between;
  padding: 10px;
  font-size:10pt;
  font-weight:bold;
  background-color: #66BB6A;
  color:white;

}

.mealItem{
  background-size:cover;
}



</style>
