<template>
<!-- Hero Section -->
<section id="hero">
  <!-- Tagline -->
  <div class="container h-100">
    <div class="row h-100">
      <div class="col-lg-6 col-sm-12 hero-tagline my-auto">
        <h1>Selamat Datang Di Website Resmi SMK Negeri 4 Tasikmalaya</h1>
        <p><span class="fw-bold"></span>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Non incidunt deserunt voluptatem fuga culpa porro consequuntur excepturi dignissimos ex ut accusamus adipisci reiciendis eligendi, provident suscipit autem recusandae mollitia aspernatur!</p>
        <button class="button-lg-secondary me-4">Lihat selengkapnya</button>
        <a href="#rekomendasi">
                        <img src="assets/Right Arrow.png" alt="">
                    </a>
      </div>
    </div>
    <img src="assets/kepala sekolah.png" class="image-hero position-absolute end-0 bottom-0" alt="" />
  </div>
</section>
<!-- End navbar -->

</template>

<style>
:root {
--pr-color: #048853;
}

body {
font-family: "Poppins", sans-serif;
background-color: #f3fff4;
}
/* Nav Fixed on Scroll */

.nav-color {
background-color: #005a36;
}

/* Nav Scroll */

.navbar {
z-index: 3;
}

nav .navbar-brand {
font-size: 20px;
font-weight: 700;
color: #fff !important;
}

.navbar .nav-link.active {
font-weight: 700;
}

.nav-link:hover {
background-color: var(--pr-color);
}

.navbar .nav-link {
font-size: 1rem;
color: #fff !important;
}

.button-primary {
width: 133px;
height: 40px;
background-color: transparent;
border: 1px solid rgba(255, 255, 255, 0.3);
font-size: 1rem;
font-weight: 500;
color: #fff;
}

.button-secondary {
width: 133px;
height: 40px;
background-color: #fff;
color: var(--pr-color);
font-size: 1rem;
font-weight: 500;
border: none;
}

.button-lg-secondary {
width: 237px;
height: 70px;
background-color: #fff;
color: var(--pr-color);
border: none;
font-size: 20px;
font-weight: 700;
}

/* Hero Section */

#hero {
background: linear-gradient(160deg, var(--pr-color), #000);
height: 100vh;
width: 100%;
}

#hero img {
z-index: 0;
}

.image-hero {
height: 100%;
}

.hero-tagline h1 {
font-size: 50px;
color: #fff;
line-height: 72px;
}

.hero-tagline p {
font-size: 1rem;
color: #fff;
margin-bottom: 60px;
margin-top: 20px;
line-height: 30px;
width: 90%;
}

* {
z-index: 2;
}

.accsent-img {
z-index: 1;
}
</style>