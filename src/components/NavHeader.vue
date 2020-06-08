<template>
  <header>
    <a id="TopNav"></a>
    <!-- Navigation -->
    <nav class="navbar navbar-expand-lg navbar-dark">
      <a class="navbar-brand mx-auto" href="#">
        <img
          src="../assets/img/headeryesdok.png"
          width="120"
          class="d-inline-block align-top"
          alt="YesDok nav image"
        />
      </a>
      <button
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        data-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav mr-auto">
          <li class="nav-item active">
            <a class="nav-link" href="#TopNav">
              Home
              <span class="sr-only">(current)</span>
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#Company">Company</a>
          </li>
          <li class="nav-item dropdown">
            <a
              class="nav-link dropdown-toggle"
              id="navbarDropdown"
              role="button"
              data-toggle="dropdown"
              aria-haspopup="true"
              aria-expanded="false"
              >Articles</a
            >
            <div class="dropdown-menu" aria-labelledby="navbarDropdown">
              <a class="dropdown-item" href="#Articles">Health A-Z</a>
              <a class="dropdown-item" href="#Articles">Parenting</a>
              <a class="dropdown-item" href="#Articles">Diet</a>
              <a class="dropdown-item" href="#Articles">Lifestyle</a>
              <a class="dropdown-item" href="#Articles">Hot</a>
              <div class="dropdown-divider"></div>
              <a class="dropdown-item" href="#Articles">COVID-19 CASES</a>
            </div>
          </li>
          <!-- <li class="nav-item">
            <a class="nav-link disabled" href="#">Download</a>
          </li>
          <li class="nav-item">
            <a class="nav-link disabled" href="#">Store</a>
          </li>
          <li class="nav-item">
            <a class="nav-link disabled" href="#">Career</a>
          </li> -->
          <li class="nav-item">
            <a class="nav-link" href="#AboutUs">About Us</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#ContactUs">Contact Us</a>
          </li>
        </ul>
        <div class="mr-2 pb-2">
          <span
            id="indonesian_language"
            class="btn btn-success "
            @click="$emit('switch-to-english', 'false')"
            v-bind:class="{ 'language-selected': !isEnglish }"
            style="background:none;border:1px solid #009CD7;border-radius:20px 0px 0px 20px;color:#009CD7;cursor:pointer;"
            >IDN
            <img
              src="../assets/img/indonesia.png"
              style="width:25px;background:none"/></span
          ><span
            id="english_language"
            class="btn btn-success "
            @click="$emit('switch-to-english', 'true')"
            v-bind:class="{ 'language-selected': isEnglish }"
            style="background:none;border:1px solid #009CD7;border-radius:0px 20px 20px 0px;color:#009CD7;cursor:pointer;"
            ><img
              src="../assets/img/english.png"
              style="width:25px;background:none"
            />
            EN</span
          >
        </div>
        <a class="btn btn-outline-warning btn-lg disabled" href="#"
          >Login / Sign Up</a
        >
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Header",
  props: {
    isEnglish: Boolean
  }
};
</script>

<style scoped>
* {
  background-color: #024668;
  font-size: 1.25rem;
}

.language-selected {
  color: white !important;
  background-color: #009cd7 !important;
}
</style>
