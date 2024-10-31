<script>
export default{
  
}
</script>

<template>
  <!-- Navbar -->
  <nav class="navbar navbar-expand-lg navbar-light bg-light shadow sticky-top">
    <div class="container-fluid">
        <a class="navbar-brand" href="/">Frando Wadino</a>
        <div class="collapse navbar-collapse d-flex justify-content-center">
            <ul class="navbar-nav mb-2 mb-lg-0">
                <li class="nav-item">
                    <a class="nav-link active" aria-current="page" href="/about">About</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link active" aria-current="page" href="/portfolio">Portfolio</a>
                </li>
            </ul>
        </div>
        <a class="btn btn-primary" href=""><span class="material-symbols-outlined">download</span>CV</a>
    </div>
</nav>

</template>

<style>
.navbar-nav {
        position: absolute;
        left: 50%;
        transform: translateX(-50%);
    };
</style>
