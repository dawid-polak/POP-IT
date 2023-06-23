<template>
     <nav class="navbar">
          <div class="navbar--logo">
               <a href=""> NOT_A_BUBBLE.COM </a>
          </div>
          <div v-if="activeMenu" class="navbar--menu">
               <ul class="navbar--menu-items">
                    <li class="item">ABOUT</li>
                    <li class="item">SALE</li>
                    <li class="item">CONTACT</li>
               </ul>
          </div>
          <div class="navbar--humburger">
               <img v-if="!activeMenu" @click="activeMenu = !activeMenu" class="humburger" src="../assets/icons/hamburger.png" alt="hamburger" />
               <img v-else @click="activeMenu = !activeMenu" class="humburger" src="../assets/icons/close.png" alt="close" />
          </div>
     </nav>
</template>

<script setup>
import { ref, onMounted } from "vue";
const activeMenu = ref(true);

onMounted(() => {
     //listener to window size
     window.addEventListener("resize", handleActiveMenu);
});

//function to change activemenu when window width is changing
const handleActiveMenu = () => {
     if (window.innerWidth > 720) {
          activeMenu.value = true;
     } else {
          activeMenu.value = false;
     }
};

//reload page when window width under 720px
if (window.innerWidth > 720) {
     activeMenu.value = true;
} else {
     activeMenu.value = false;
}
</script>

<style scoped>
.navbar {
     position: absolute;
     top: 0;
     height: 80px;
     width: 100vw;
     display: flex;
     align-items: center;
     font-size: 18px;
}

.navbar--logo {
     flex-grow: 1;
     margin-left: 70px;
}

.navbar--logo a {
     font-weight: 700;
     text-decoration: none;
     color: black;
}

.navbar--menu {
     margin-right: 70px;
     display: block;
}

.navbar--menu-items {
     display: flex;
     list-style: none;
}

.navbar--menu-items .item {
     margin-right: 50px;
}

.navbar--menu-items .item:hover {
     cursor: pointer;
     color: #6a6a6a;
}

.navbar--humburger {
     margin-right: 70px;
     display: none;
}

.navbar--humburger .humburger {
     width: 25px;
     height: 25px;
}

.navbar--humburger .humburger:hover {
     cursor: pointer;
     color: #6a6a6a;
}

/* breakpoints */
@media only screen and (max-width: 720px) {
     .navbar--humburger {
          display: block;
     }

     .navbar--menu {
          position: absolute;
          margin: 190px 0px 0px 0px;
          width: 100vw;
          text-align: center;
     }

     .navbar--menu-items {
          flex-flow: column;
          margin: auto;
     }

     .navbar--menu-items .item {
          padding: 10px;
     }
}
</style>
