<script>
document.addEventListener('DOMContentLoaded', function () {
  var menuIcon = document.querySelector('.menu-icon');

  menuIcon.addEventListener('click', function () {
    this.classList.toggle('active');
  });
});

</script>

<template>

  <nav class="navbar position-absolute w-100 navbar-expand-lg z-3">
    <div class="container-fluid">
      <a class="navbar-brand ps-sm-5 ps-2" href="#"><img src="/icon.png" width="40"></a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
        aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">

        <div class="menu-icon">
          <div class="line line-1"></div>
          <div class="line line-2"></div>
          <div class="line line-3"></div>
        </div>

      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav w-100">
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
    </div>
  </nav>
</template>

<style scoped>
.navbar-toggler,
.navbar-toggler-icon {
  border: none !important;
}

.navbar-toggler:focus {
  outline: none;
  box-shadow: none;
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

.navbar-nav {
  height: 10vh;
  justify-content: center;
  align-items: center;
}

.nav-link {
  color: azure !important;
}

@media (max-width: 728px) {
  .navbar-nav {
    height: 100vh;
  }

  .icons {
    display: block !important;
  }

}
</style>