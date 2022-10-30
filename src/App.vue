<script setup>
import { RouterLink, RouterView } from "vue-router";
import HelloWorld from "./components/HelloWorld.vue";
import ol from './assets/Images/img6.png'
import Asa from './assets/Images/img4.png'
import Lay from './assets/Images/img1.png'
import Buju from './assets/Images/img7.png'
</script>

<template>
  <header>
    <div className="container">
      <div className="navflex">
        <div className="flogow">
          <img src="./assets/Images/mctlogo.png" />
        </div>
        <div className="navlinks">
          <ul>
            <li><RouterLink to="/">Home</RouterLink></li>
            <li><RouterLink to="/about">Music</RouterLink></li>
            <li><RouterLink to="/about">Movieszz</RouterLink></li>
            <li><RouterLink to="/about">Theatre/Comedy</RouterLink></li>
            <li><RouterLink to="/about">Sports</RouterLink></li>
            <li><RouterLink to="/about">Contact Us</RouterLink></li>
          </ul>
        </div>
        <div>
          <button className="btn">
            <router-link to="/mycart"> My cart </router-link>
          </button>
        </div>
      </div>
    </div>
  </header>

  <RouterView :myproducts="products" />
</template>

<script>
export default {
  setup() {
        const imageUrl = new URL("../assets/images/", import.meta.url).href;
        return { imageUrl };
    },
  data() {
    return {
      products: [
        {
          Img: ol,
          Name: "ASA LIVE IN CONCERT",
          Date: "December 15 @6:30pm",
          Description: "Genesis Event Center, Lagos, Nigeria.",
        },
        {
          Img: Asa,
          "Name": "ASA LIVE IN CONCERT AT 02 ARENA ",
          "Date": "June 15 @6:30pm",
          "Description": "Genesis Event Center, Lagos, Nigeria. anywhere you see canpy, just come first ",
        },
         {
          Img:Lay,
          Name: "ASA LIVE IN CONCERT",
          Date: "June 15 @6:30pm",
          Description: "Genesis Event Center, Lagos, Nigeria.",
        },
         {
          Img: Buju,
          Name: "ASA LIVE IN CONCERT",
          Date: "June 15 @6:30pm",
          Description: "Genesis Event Center, Lagos, Nigeria.",
        },
          {
          Img: ol,
          Name: "ASA LIVE IN CONCERT",
          Date: "June 15 @6:30pm",
          Description: "Genesis Event Center, Lagos, Nigeria.",
        },
        {
          Img: Asa,
          "Name": "ASA LIVE IN CONCERT",
          "Date": "June 15 @6:30pm",
          "Description": "Genesis Event Center, Lagos, Nigeria.",
        },
         {
          Img:Lay,
          Name: "ASA LIVE IN CONCERT",
          Date: "June 15 @6:30pm",
          Description: "Genesis Event Center, Lagos, Nigeria.",
        },
         {
          Img: Buju,
          Name: "ASA LIVE IN CONCERT",
          Date: "June 15 @6:30pm",
          Description: "Genesis Event Center, Lagos, Nigeria.",
        }
      ],
    };
  },
};
</script>
<style src="@/assets/style.css"></style>
