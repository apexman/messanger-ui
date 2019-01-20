<template>
    <div>
        <LeftSideHeader></LeftSideHeader>
        <LeftSideChatsList
                v-on:onChatClick="onChatClick"
                :chats="chats"></LeftSideChatsList>
    </div>
</template>

<script>
    import LeftSideHeader from "./LeftSideHeader";
    import LeftSideChatsList from "./LeftSideChatsList";
    export default {
        name: "LeftSide",
        components: {LeftSideChatsList, LeftSideHeader},
        props: [
            "chats"
        ],
        methods: {
            onChatClick(chat) {
                this.$emit("onChatClick", chat)
            }
        }
    }
</script>

<style scoped>

</style>