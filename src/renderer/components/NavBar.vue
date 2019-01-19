<template>
    <div>
        <nav class="navbar is-dark" role="navigation" aria-label="dropdown navigation">
            <div class="navbar-brand">
                <a class="navbar-item not-affect" href="/#/">
                    <!-- <img :src="logo" alt="Book Reads" width="112" height="28"> -->
                    <span><i class="mdi mdi-24px mdi-home"></i> Home</span>
                </a>
                <div class="navbar-burger burger" v-on:click="showNav = !showNav"
                     v-bind:class="{ 'is-active' : showNav }" data-target="navbarExampleTransparentExample">
                    <span></span>
                    <span></span>
                    <span></span>
                </div>
            </div>
            <div class="navbar-menu" v-bind:class="{ 'is-active' : showNav }">
                <div class="navbar-start">
                    <a class="navbar-item">
                        <span><i class="mdi mdi-24px mdi-library-books"></i> Books</span>
                    </a>
                    <a class="navbar-item">
                        <span><i class="mdi mdi-24px mdi-comment-text-outline"></i> Book Reviews</span>
                    </a>
                    <a class="navbar-item">
                        <span><i class="mdi mdi-24px mdi-account-multiple"></i> Users</span>
                    </a>
                    <div class="navbar-item has-dropdown is-hoverable" @click="showSubMenu()">
                        <a class="navbar-link"><span><i class="mdi mdi-24px mdi-view-list"></i> Books</span></a>
                        <div class="navbar-dropdown is-hidden-touch">
                            <a class="navbar-item" href=""><span><i class="mdi mdi-24px mdi-star"></i> Favorites</span></a>
                        </div>
                    </div>
                </div>
                <div class="navbar-end">
                    <a v-if="navLogin" class="navbar-item" @click="openLogin()">
                        Login
                    </a>
                    <router-link v-if="navLogin" class="navbar-item" to="/register">Signup!</router-link>
                    <!-- <div class="navbar-item ">
                        <div class="field is-grouped">
                            <p class="control">
                                <router-link class="button is-outlined" to="/add-book">
                                    <span>Add New Book</span>
                                </router-link>
                            </p>
                        </div>
                    </div> -->
                </div>
            </div>
        </nav>
    </div>
</template>

<script>
  export default {
    name: 'NavBar'
  }
</script>

<style scoped>

</style>