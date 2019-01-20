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
    export default {
        name: "RightSideInputForm",
        props: [
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
                this.messages.push({id: this.text, text: this.text});
            }
        }
    }
</script>

<style scoped>
    /*.input-group {*/
        /*display: inline;*/
    /*}*/
</style>