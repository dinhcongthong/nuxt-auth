<template>
  <div class="root">
    <nav class="navbar navbar-expand-lg bg-light">
      <div class="container-fluid">
        <a class="navbar-brand fw-bold" href="#">NUXT API</a>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarNavDropdown"
          aria-controls="navbarNavDropdown"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNavDropdown">
          <ul class="navbar-nav">
            <li class="nav-item">
              <NuxtLink
                to="/dashboard"
                class="nav-link"
                aria-current="page"
                exact
              >
                Home page
              </NuxtLink>
            </li>
            <li class="nav-item">
              <NuxtLink
                to="/dashboard/about"
                class="nav-link"
                aria-current="page"
              >
                About page
              </NuxtLink>
            </li>
            <li class="nav-item dropdown">
              <a
                class="nav-link dropdown-toggle"
                href="#"
                role="button"
                data-bs-toggle="dropdown"
                aria-expanded="false"
              >
                User
              </a>
              <ul class="dropdown-menu">
                <li>
                    <nuxt-link to="/login" class="dropdown-item">
                        Login
                    </nuxt-link>
                    </li>
                <li><a class="dropdown-item" href="#">Profile</a></li>
                <li>
                  <a class="dropdown-item" href="#">Logout</a>
                </li>
              </ul>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <Nuxt />
  </div>
</template>

<script>
export default {
  head: {
    script: [
      {
        src: "https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.bundle.min.js",
      },
    ],
  },
};
</script>

<style>
@import "~/assets/style/app.css";
a,
.nav-link {
  text-decoration: none;
  color: black;
}
a,
.nav-link:hove {
  color: black;
}
.nuxt-link-exact-active {
  font-weight: bold;
}
</style>