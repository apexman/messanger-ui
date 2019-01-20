<template>
    <!--<b-container>-->
        <!--<b-row no-gutters align-v="center">-->
            <!--<b-col md="auto" class="img-cls mr-3">-->
                <!--<img src="../../assets/chat1.png" class="rounded-circle" style="width: 75px; height: 75px;"/>-->
            <!--</b-col>-->
            <!--<b-col class="message d-flex">-->
                <!--<div class="mr-auto">-->
                    <!--{{ message }}-->
                <!--</div>-->
                <!--<div>time is now</div>-->
            <!--</b-col>-->
        <!--</b-row>-->
    <!--</b-container>-->

    <!--<b-form-textarea class="" plaintext :value="message" no-resize></b-form-textarea>-->

    <div class="d-flex ">
        <div class="d-inline-flex mr-2">
            <img src="../../assets/chat1.png" class="rounded-circle" style="width: 75px; height: 75px;"/>
        </div>
        <div class="d-flex  mr-auto message-text p-1 border border-primary rounded"> {{ message }}</div>
        <!--<b-form-textarea class="message-text align-self-stretch" autocomplete plaintext :value="message" no-resize></b-form-textarea>-->
        <div class="message-time">time to start</div>
    </div>
</template>

<script>
    export default {
        name: "Message",
        props: [
            "message"
        ]
    }
</script>

<style scoped>
    .message {
        text-align: left;
    }

    .message-text {
        text-align: left;
        /*border: black 1px solid;*/
        width: 100%;
    }

    .message-time {
        min-width: 75px;
        max-width: 75px;
    }
</style>