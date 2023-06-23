<template>
     <header class="welcome">
          <div class="welcome--content">
               <h1>POP IT!</h1>
               <h5>
                    Best Antistress Toy is the Endless toy <br />
                    bubble wrap!
               </h5>
               <button class="welcome--content-btn">BUY</button>
          </div>
          <img class="welcome--bg" src="../assets/img/background.png" alt="background" />
     </header>
</template>

<script setup></script>

<style scoped>
.welcome {
     width: 100vw;
     height: 100vh;
}

.welcome .welcome--bg {
     width: 100%;
     height: 100%;
     object-fit: cover;
}

.welcome .welcome--content {
     position: absolute;
     height: 100vh;
     display: flex;
     flex-flow: column;
     justify-content: center;
     color: #fff;
     margin-left: 100px;
}

.welcome .welcome--content h1 {
     font-size: 200px;
     margin: 0;
}

.welcome .welcome--content h5 {
     font-size: 30px;
     margin: 0;
     font-weight: 400;
}

.welcome .welcome--content .welcome--content-btn {
     max-width: 250px;
     height: 50px;
     background-color: #cbf3f0;
     border: 0;
     font-size: 20px;
     font-weight: 600;
     margin-top: 80px;
     color: #000;
     cursor: pointer;
}


/* breakpoints */
@media only screen and (max-width: 820px) {
     .welcome .welcome--content {
          margin-left: 40px;
     }

     .welcome .welcome--content h1 {
          font-size: 100px;
     }

     .welcome .welcome--content h5 {
          font-size: 15px;
     }

     .welcome .welcome--content .welcome--content-btn {
          max-width: 200px;
     }
}

@media only screen and (max-width: 420px) {
     .welcome .welcome--content h1 {
          font-size: 80px;
     }
}
</style>
