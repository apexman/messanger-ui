<template>
    <div>
        <b-list-group class="message-list">
            <!--<b-list-group-item flush class="flex-column">-->
                <!--<Message :message="message1"></Message>-->
            <!--</b-list-group-item>-->
            <!--<b-list-group-item flush>-->
                <!--<Message :message="message2"></Message>-->
            <!--</b-list-group-item>-->
            <b-list-group-item v-for="message in messages">
                <Message :message="message.text"></Message>
            </b-list-group-item>
        </b-list-group>
    </div>
</template>

<script>
    import Message from "./Message";
    export default {
        name: "RightSideMessagesList",
        components: {Message},
        props: [
            "messages"
        ],
        data() {
            return {
                message1: "МЕСССАААГАААА dddddddddddd dddddddddddddddddddddddddd dddddddddddddddddddddddddddddddd ddddddddddddddddddddd dddddddddddddddddddd dddddddddddd" +
                "МЕСССАААГАААА dddddddddddd dddddddddddddddddddddddddd dddddddddddddddddddddddddddddddd ddddddddddddddddddddd dddddddddddddddddddd dddddddddddd" +
                "МЕСССАААГАААА dddddddddddd dddddddddddddddddddddddddd dddddddddddddddddddddddddddddddd ddddddddddddddddddddd dddddddddddddddddddd dddddddddddd",
                message2: "ФФФФФФФФФФФФААААААААААААААААААААААРШ",
            }
        }
    }
</script>

<style scoped>
    .message-list {
        overflow-y: auto;
    }
</style>