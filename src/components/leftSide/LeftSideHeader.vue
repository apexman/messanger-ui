<template>
    <div class="left-side-header d-flex align-items-center">
        <img
                class="mr-2"
                @click="hamburgerHandler"
                src="../../assets/HamburgerMenu.svg">
        <span>App name</span>
    </div>
</template>

<script>
    export default {
        name: "LeftSideHeader",
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