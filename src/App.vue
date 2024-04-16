<template>
    <div class="main">
        <Navbar :logo="logo_src" :alt="app_name" />
        <div class="content">
            <router-view />
        </div>
        <Footer />
    </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Footer from "./components/Footer.vue";

export default {
    components: {
        Navbar,
        Footer,
    },
    data() {
        return {
            logo_src: "/img/logo.png",
            app_name: "Make your burger",
        };
    },
};
</script>

<style>
* {
    font-family: Helvetica;
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}

.main {
    min-height: 100vh;

    display: flex;
    flex-direction: column;
    justify-content: space-between;
}

.main .content {
    flex-grow: 1;
}

.main-container {
    margin: 50px;
    min-height: 250px;
}

h1 {
    text-align: center;
    font-size: 42px;
    margin-bottom: 30px;
    color: #222;
}
</style>
