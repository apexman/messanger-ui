<template>
    <div>
        <b-container>
            <b-row no-gutters align-v="center">
                <b-col md="auto" class="mr-3">
                    <img class="chat-img rounded-circle" src="../../assets/chat1.png"/>
                </b-col>
                <b-col class="chat-preview">
                    <div>
                        <div class="d-flex justify-content-between align-items-center">
                            <strong>{{ chat.name }}</strong>
                            <b-badge variant="dark" pill>{{ chat.lastMessage.time }}</b-badge>
                        </div>
                        <div class="d-flex justify-content-between align-items-center">
                            {{ chat.lastMessage.text }}
                            <b-badge pill variant="success">{{ chat.unreadMessagesCount }}</b-badge>
                        </div>
                    </div>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>

<script>
    export default {
        name: "ChatPreview",
        props: {
            chat: {
                type: Object,
                required: false,
            }
        },
    }
</script>

<style scoped>
    .chat-img {
        width: 75px; height: 75px;
    }

    .chat-preview {
        text-align: left;
        width: 100%;
    }
</style>