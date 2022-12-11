<template>
  <footer class="footer">
  <div class="wraper-footer">
    <div class="football-school">
      <a href="#">
        <img src="/svg/footlogo.png" alt="football-school">
      </a>
    </div>
    <div class="year">
      <span>2022</span>
    </div>
    <div class="github">
      <a href="https://github.com/FoxyRommel/footbalclub.git">
        <img src="/svg/github-logo.svg" alt="github">
      </a>
    </div>
  </div>          
  </footer>
  </template>

<script>

</script>

<style scoped>
  .footer {
    width: 100%;
    margin-top: 50px;
    margin-top: auto;
    background-color: #0033a1
  }
  .wraper-footer {
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding: 10px;
  }
  .fooball-shool {
    max-width: 100px;
    height: 50px;
  }
  .github a img {
    width: 45px;
  }
  .football-school a img {
    width: 45px;
  }
  
</style>