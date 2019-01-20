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
                            <strong>Chat name</strong>
                            <b-badge variant="dark" pill>3 days ago</b-badge>
                        </div>
                        <div class="d-flex justify-content-between align-items-center">
                            Chat's last message
                            <b-badge pill variant="success">15</b-badge>
                        </div>
                    </div>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>

<script>
    export default {
        name: "ChatPreview"
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