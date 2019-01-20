<template>
    <div>
        <!--<input class="mb-2" value="Search" />-->

        <b-input-group class="mb-3">
            <b-form-input
                    placeholder="Search"
                    v-model.trim="searchInAllChats"></b-form-input>
            <!--<b-input-group-append>-->
                <!--<b-btn @click="">Search</b-btn>-->
            <!--</b-input-group-append>-->
        </b-input-group>

        <b-list-group>
            <b-list-group-item
                    v-for="chat in chats"
                    :key="chat.id"
                    @click="clickedChat(chat)"
                    button
                    class="pl-0 pr-0">
                <ChatPreview
                        :chat="chat"></ChatPreview>
            </b-list-group-item>
        </b-list-group>
    </div>
</template>

<script>
    import ChatPreview from "./ChatPreview";
    export default {
        name: "LeftSideChatsList",
        props: [
            "chats"
        ],
        data() {
            return {
                searchInAllChats: ""
            }
        },
        components: {ChatPreview},
        methods: {
            clickedChat(chat) {
                this.$emit("onChatClick", chat);
            }
        }
    }
</script>

<style scoped>

</style>