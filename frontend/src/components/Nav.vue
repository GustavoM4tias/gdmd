<script>
document.addEventListener('DOMContentLoaded', function () {
  var menuIcon = document.querySelector('.menu-icon');
  var navbar = document.querySelector('.navbar');

  // Toggle active state of the menu icon
  menuIcon.addEventListener('click', function () {
    this.classList.toggle('active');
  });

  // Detect scroll and adjust navbar size
  window.addEventListener('scroll', function () {
    if (window.scrollY > window.innerHeight * 0.5) { // Verifica se a rolagem passou de 50% da altura da janela
      navbar.classList.add('navbar-small');
    } else {
      navbar.classList.remove('navbar-small');
    }
  });
});
</script>




<template>
  <nav class="navbar container-fluid fixed-top navbar-expand-lg z-3">
    <a class="navbar-brand ps-sm-5 ps-2" href="#">
      <img src="/icon.png" class="img-logo mt-1 ms-0 ms-md-5">
    </a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
      aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
      <div class="menu-icon">
        <div class="line line-1"></div>
        <div class="line line-2"></div>
        <div class="line line-3"></div>
      </div>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Features</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Pricing</a>
        </li>
        <li class="nav-item icons d-none">
          <i class="fa-brands fa-instagram px-2"></i>
          <i class="fa-brands fa-linkedin px-2"></i>
          <i class="fa-brands fa-github px-2"></i>
        </li>
      </ul>
    </div>
  </nav>
</template>

<style scoped>
.navbar {
  position: fixed;
  top: 0;
  background-color: rgba(0, 0, 0, 0.15);
  z-index: 900;
  box-shadow: 0 0 50px rgba(0, 0, 0, .3);
  transition: height 0.3s ease-in-out, padding 0.3s ease-in-out;
  height: 10vh;
  padding: 10px 0;
  transition: .6s;
}

.navbar-small {
  height: 8vh;
  padding: 5px 0;
  transition: .6s;

  & .img-logo {
    height: 7vh;
    transition: .6s;
  }

}

.navbar-toggler,
.navbar-toggler-icon {
  border: none !important;
}

.navbar-toggler:focus {
  outline: none;
  box-shadow: none;
}

.img-logo {
  height: 9vh;
  transition: .6s;
}

.menu-icon {
  width: 50px;
  height: 50px;
  cursor: pointer;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-around;
}

.line {
  width: 100%;
  height: 8px;
  background-color: #fff;
  border-radius: 3px;
  box-shadow: 0 2px 10px 0 rgba(0, 0, 0, 0.3);
  transition: transform 0.3s ease-in-out, opacity 0.2s ease-in-out;
}

.menu-icon.active .line-1 {
  transform: translateY(10px) rotate(45deg);
}

.menu-icon.active .line-2 {
  transform: scaleX(0);
  opacity: 0;
}

.menu-icon.active .line-3 {
  transform: translateY(-25px) rotate(-45deg);
}

.collapse {
  justify-content: center;
  align-items: center;
  width: 100vw;
}

.navbar-nav {
  margin-right: 150px;
}

.nav-link {
  color: azure !important;
}


@media (max-width: 728px) {
  .navbar-nav {
    background-color: red;
    margin-top: -12vh !important;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: auto;
  }

  .nav-link {
    color: rgb(0, 0, 0) !important;
  }

  .icons {
    display: block !important;
  }
}
</style>
