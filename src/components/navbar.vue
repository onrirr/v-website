<script lang="ts">
//@ts-nocheck 
document.addEventListener('DOMContentLoaded', () => {

const $navbarBurgers = Array.prototype.slice.call(document.querySelectorAll('.navbar-burger'), 0);

$navbarBurgers.forEach( el => {
  el.addEventListener('click', () => {
    const target = el.dataset.target;
    const $target = document.getElementById(target);
    el.classList.toggle('is-active');
    $target.classList.toggle('is-active');

  });
});

});



export default {}
</script>
<template>
   
    <nav class="navbar" role="navigation" aria-label="main navigation">
  <div class="navbar-brand">
    <a class="navbar-item" href="/">
      <img src="https://vlang.io/img/v-logo.png" width="32" height="32"/>
    </a>

    <a role="button" class="navbar-burger" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample">
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
    </a>
  </div>

  <div id="navbarBasicExample" class="navbar-menu">
    <div class="navbar-start">
      <a class="navbar-item">
        Home
      </a>

      <a class="navbar-item">
        Documentation
      </a>

      <div class="navbar-item has-dropdown is-hoverable">
        <a class="navbar-link">
          More
        </a>

        <div class="navbar-dropdown">
          <a class="navbar-item">
            About
          </a>
          <a class="navbar-item">
            Tutorials
          </a>
          <a class="navbar-item">
            Blog
          </a>
          <a class="navbar-item">
            Forum
          </a>
          <a class="navbar-item">
            V Package Manager
          </a>
          <hr class="navbar-divider"/>
          <a class="navbar-item">
            Contribute on Github
          </a>
        </div>
      </div>
    </div>

    <div class="navbar-end">
      <div class="navbar-item">
        <div class="buttons">
          <a class="button">
            <strong>Support V</strong>
          </a>
          <a class="button">
            Contribute
          </a>
        </div>
      </div>
    </div>
  </div>
</nav>



</template>
