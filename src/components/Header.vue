<template>
  <header class="header">
   <h1 class="header-logo">Crush 40</h1>
    <div class="buttons">
      <button class="button">Login</button>
      <button class="button">Register</button>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
}
</script>

<style>

p{
  font-family: 'Inter', sans-serif;
}
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1em;
  height: 50px;
  position:sticky;
  top:0;
  z-index: 10;
  background-color:#0a0528;
  border-bottom: 4px solid #12fcff;
  border-right: 4px solid #12fcff;
  border-left: 4px solid #12fcff;
  border-radius: 5px;
}
.header-logo{
  font-family: 'Inter', sans-serif;
  font-size: 3em;
  font-style: italic;
  font-weight: bolder;
  color: #23012f;
  -webkit-text-stroke: 2px #12fcff;
  text-shadow: 
      0 0 2px #00d5ff,
      0 0 5px #00d5ff,
      0 0 7px #00d5ff,
      0 0 10px #00d5ff,
      0 0 12px #00d5ff,
      0 0 15px #00d5ff,
      0 0 17px #00d5ff;
}
.buttons{
  display: flex;
  
}
.button{
  margin-left: 1em;
  padding: 0.5em 1em;
  border-radius: 0.25em;
  border: 2px solid #12fcff;
  background: linear-gradient(#540071, #23012f);    cursor: pointer;
  cursor: pointer;
  box-shadow: 
      0 0 5px #00d5ff,
      0 0 10px #00d5ff,
      inset 0 0 5px #00d5ff,
      inset 0 0 10px #00d5ff;
      transition: border 0.3s, box-shadow 0.3s;

}
.button:hover {
  background: linear-gradient(#9500c0, #610081);
  transition-duration: 0.5s;
  border: 4px solid #8500b2;
  box-shadow: 
        0 0 10px #8500b2,
        0 0 20px #8500b2,
        inset 0 0 10px #8500b2,
        inset 0 0 20px #8500b2;
  transition: 0.3s; 
}
</style>