<script>
import { RouterLink } from 'vue-router';

export default{
    data(){
        return{
            activeTab: 'tab4'
        }
    }
}
</script>

<template>
  <!-- Navbar -->
  <nav class="navbar navbar-expand-lg navbar-light bg-light shadow sticky-top">
    <div class="container-fluid">
        <router-link class="navbar-brand" href="/">FW</router-link>
        <div class="collapse navbar-collapse d-flex justify-content-center">
            <ul class="navbar-nav mb-2 mb-lg-0">
                <li class="nav-item">
                    <router-link class="nav-link" :class="{active: activeTab === 'tab1'}" @click="activeTab = 'tab1'" to="/">Home</router-link>
                </li>
                <li class="nav-item">
                    <router-link class="nav-link" :class="{active: activeTab === 'tab2'}" @click="activeTab = 'tab2'" to="/about">About</router-link>
                </li>
                <li class="nav-item">
                    <router-link class="nav-link" :class="{active: activeTab === 'tab3'}" @click="activeTab = 'tab3'" to="/portfolio">Portfolio</router-link>
                </li>
            </ul>
        </div>
        <button class="btn btn-primary" @click=""><span class="material-symbols-outlined">download</span>CV</button>
    </div>
</nav>

</template>

<style>
.navbar-nav {
        position: absolute;
        left: 50%;
        transform: translateX(-50%);
    }

.nav-link.active{
        text-decoration: underline;
    }
</style>
