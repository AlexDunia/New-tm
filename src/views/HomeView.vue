<script setup>
import TheWelcome from "../components/TheWelcome.vue";
import Bg from '../assets/Images/crowd.jpg'
</script>

<template>
 


      <div class="spacearound">
        <img src="../assets/Images/fboyb.jpg"/>
      </div>

      
   
        <div className="latest"> <h1> Latest events </h1> </div>
         
         <div class="circular"
       :style="{ backgroundImage: 'url(' + image + ')' }">
        <div className="t_grids">


      <div className="one_e" v-for="(oneticket, i) in myproducts" :key="i"> 
      <ul> 
      <li className="mypimage"> <img :src="oneticket.Img"/> </li>
        <li className="noe"> {{ oneticket.Name }} </li>
          <div className="toe"> <i class="fa-solid fa-location-dot"> </i>   {{ oneticket.Description }}  </div> 
        
         <div className="toe"> <i class="fa-solid fa-calendar-days"></i> {{ oneticket.Date }} </div> 
       
        
        <li className="toe"> {{ oneticket.Price }} </li>
        <button className="b_t"> Buy Ticket </button> 
        </ul>
      </div>
 
      </div>
       </div>
    
   <div className="cdtext"> <h1> 15 </h1> </div> 
   <div> className="cdtext" <h2> Days </h2> </div> 
   <div> <h2> TO GO </h2> </div> 
  

</template>

<script>
export default {
props: ['myproducts'],
data() {
  return{
     image: Bg
  }
}
}
</script>
