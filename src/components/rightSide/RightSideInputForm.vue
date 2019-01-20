<template>
    <div class="input-group">
        <b-button>Attachment</b-button>
        <b-form-textarea v-model="text"
                         placeholder="Write a message, plz..."
                         no-resize
                         :rows="3" >
        </b-form-textarea>
        <b-button>smiles</b-button>
        <b-button @click="sendMessage">Sent</b-button>
    </div>
</template>

<script>
    import axios from "axios";

    export default {
        name: "RightSideInputForm",
        props: [
            "chat",
            "messages"
        ],
        data() {
            return {
                text: ""
            }
        },
        methods: {
            sendMessage(){
                console.log("sendMessage");
                if (this.text && this.text.trim() !== "") {
                    this.messages.push({id: this.text, text: this.text});

                    // axios.post("/chat", {chatId: this.chat.id, text: this.text})
                    //     .then(function (response) {
                    //         console.log(response);
                    //     })
                    //     .catch(function (error) {
                    //         console.log(error);
                    //     });
                }
            },
        }
    }
</script>

<style scoped>
    /*.input-group {*/
        /*display: inline;*/
    /*}*/
</style>