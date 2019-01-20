<template>
    <div class="left-side-header d-flex align-items-center">
        <img
                class="mr-2"
                @click="hamburgerHandler"
                src="../../assets/HamburgerMenu.svg">
        <!--<HamburgerMenu></HamburgerMenu>-->
        <!--<b-navbar-toggle target="nav_collapse"></b-navbar-toggle>-->
        <span>App name</span>
    </div>
</template>

<script>
    import HamburgerMenu from "./HamburgerMenu";
    export default {
        name: "LeftSideHeader",
        components: {HamburgerMenu},
        methods: {
            hamburgerHandler(){
                alert("Hamburger Alert");
            }
        }
    }
</script>

<style scoped>
    .left-side-header {
        min-height: 40px;
        /*text-align: left;*/
    }
</style>