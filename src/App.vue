<template>
     <Navbar />
     <Welcome />
     <section id="about">
          <h1>What is Pop it exactly?</h1>
          <p>This is a child game, in which the process can be compared to the burstring of a bubble wrap. But unlike film, pop-it can be pressed with the seme characteristic sensations and sounds "endlessy": dozens of silicone bubbles are simply squeezed out in the other direction.</p>
     </section>
     <section id="choose">
          <h1>Choose your Pop-It!</h1>
          <div class="choose--items">
               <ChooseItem v-for="item in choose_items" :key="item.id" :data="item" />
          </div>
     </section>
     <Rules />
     <Footer />
</template>
<script setup>
import Navbar from "./components/Navbar.vue";
import Welcome from "./components/Welcome.vue";
import ChooseItem from "./components/ChooseItem.vue";
import Rules from "./components/Rules.vue";
import Footer from "./components/Footer.vue"

const choose_items = [
     {
          id: 0,
          description: "Multicolored square",
          img_src: "/src/assets/img/square.png",
          img_name: "square",
     },
     {
          id: 1,
          description: "Amoung Us, marbled",
          img_src: "/src/assets/img/amongus.png",
          img_name: "amongus",
     },
     {
          id: 2,
          description: "Multicolored round",
          img_src: "/src/assets/img/round.png",
          img_name: "round",
     },
];
</script>

<style scoped>
/* SECTION ABOUT */
#about {
     width: 100%;
     text-align: center;
     padding: 100px 0px;
     display: flex;
     flex-flow: column;
     align-items: center;
     justify-content: center;
}

#about h1 {
     font-size: 30px;
     font-weight: 800;
     margin: 0;
}

#about p {
     font-size: 20px;
     font-weight: 100;
     max-width: 60%;
     margin: 20px 0px 0px 0px;
}

/* SECTION CHOOSE */
#choose {
     width: 100%;
     background-color: #cbf3f0;
}

#choose h1 {
     font-size: 30px;
     font-weight: 800;
     margin: 0;
     padding-top: 100px;
     text-align: center;
}

#choose .choose--items {
     display: flex;
     justify-content: space-around;
     flex-wrap: wrap;
     width: 80vw;
     padding: 50px 0px 100px 0px;
     margin: auto;
}

/* breakpoints */
@media only screen and (max-width: 720px) {
     /* section about */
     #about h1 {
          font-size: 25px;
     }

     #about p {
          font-size: 18px;
     }
}
</style>
