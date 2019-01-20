<template>
    <div class="right-side-header d-flex align-items-center">
        <div class="mr-auto">
            App name
            <small class="app-descr">service to chat ahahahahaha</small>
        </div>
        <!--<b-input-group>-->
            <!--<b-form-input />-->
            <!--<b-input-group-append>-->
                <!--<b-btn size="sm" text="Search" variant="success">Search</b-btn>-->
            <!--</b-input-group-append>-->
        <!--</b-input-group>-->
        <!--<b-button class="mr-2">Search</b-button>-->
        <div class="right-menu"></div>
    </div>
</template>

<script>
    export default {
        name: "RightSideHeader"
    }
</script>

<style scoped>
    .right-side-header {
        min-height: 40px;
        display: inline;
        text-align: left;
    }

    .app-descr {
        font-style: italic;
        font-size: 75%;
    }

    .right-menu:after {
        content: '\2807';
        font-size: 20px;
    }
</style>