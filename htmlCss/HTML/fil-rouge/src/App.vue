<template>
<div class="container">
<div class="ftp">
  <img class="livreTopFlop" src="./assets/L-Etranger.jpg" alt="bouquin">
  <p class="annonce">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam iaculis leo nunc. Etiam sagittis erat at turpis venenatis, eget porttitor massa convallis....</p>
  <div class="note"><h1>10</h1></div>
  <button class="button-18" role="button">Voir les moins bonnes notes</button>
</div>
<div class="menuD">
<div class="menuProfil"></div>
</div>
<div class="navBar">
</div>
</div>
</template>

<script>
export default {
}
</script>

<style>
.container {
  height: 100%;
  display: grid; 
  grid-template-columns: 1fr 1fr 1fr; 
  grid-template-rows: 1.3fr 1.3fr 0.4fr; 
  gap: 0px 0px; 
  grid-template-areas: 
    "top top top"
    "carousel carousel carousel"
    "navBar navBar navBar"; 
}
.navBar{
  grid-area: navBar;
  background-color: #336DBF;
  display: grid; 
  grid-template-columns: 1fr 1fr 1fr 1fr; 
  gap: 0px 0px; 
  grid-template-areas: 
    ". . . ."; 
}
.ftp{
  grid-area: top;
  display: grid; 
  grid-template-columns: 1.3fr 0.9fr 0.8fr; 
  grid-template-rows: 2fr 1fr 0.5fr; 
  gap: 0px 0px; 
  grid-template-areas: 
    "livre textetop textetop"
    "livre note ."
    "nav nav nav";  
}
.menuD{
  grid-area: carousel;
}
.livreTopFlop{
  grid-area: livre;
  margin-left: 13px;
  margin-top: 45px;
}
.annonce{
  grid-area: textetop;
  margin-left: 10px;
  margin-top: 45px;
}
.note{
  border-radius: 50%;
  background-color: #38BD36;
  grid-template-areas:note;
  height: 70px;
  width: 70px;
  text-align: center;
  margin:13px;
  box-shadow:2px 5px 16px 0px #0B325E;
}
  .button-18 {
  grid-area: nav;
  align-items: center;
  background-color: #336DBF;
  border: 0;
  border-radius: 100px;
  box-sizing: border-box;
  color: #ffffff;
  cursor: pointer;
  display: inline-flex;
  font-family: -apple-system, system-ui, system-ui, "Segoe UI", Roboto, "Helvetica Neue", "Fira Sans", Ubuntu, Oxygen, "Oxygen Sans", Cantarell, "Droid Sans", "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Lucida Grande", Helvetica, Arial, sans-serif;
  font-size: 16px;
  font-weight: 600;
  justify-content: center;
  line-height: 20px;
  max-width: 480px;
  min-height: 40px;
  min-width: 0px;
  overflow: hidden;
  padding: 0px;
  padding-left: 20px;
  padding-right: 20px;
  margin-left: 15%;
  margin-right: 15%;
  text-align: center;
  touch-action: manipulation;
  transition: background-color 0.167s cubic-bezier(0.4, 0, 0.2, 1) 0s, box-shadow 0.167s cubic-bezier(0.4, 0, 0.2, 1) 0s, color 0.167s cubic-bezier(0.4, 0, 0.2, 1) 0s;
  user-select: none;
  -webkit-user-select: none;
  vertical-align: middle;
}

.button-18:hover,
.button-18:focus { 
  background-color: #16437E;
  color: #ffffff;
}

.button-18:active {
  background: #09223b;
  color: rgb(255, 255, 255, .7);
}

.button-18:disabled { 
  cursor: not-allowed;
  background: rgba(0, 0, 0, .08);
  color: rgba(0, 0, 0, .3);
}
.menuProfil{
  display: grid; 
  grid-template-columns: 0.5fr 1.5fr 1fr; 
  grid-template-rows: 0.8fr 0.3fr 1.9fr; 
  gap: 0px 0px; 
  grid-template-areas: 
    ". . ."
    ". . ."
    ". . ."; 
}
</style>
