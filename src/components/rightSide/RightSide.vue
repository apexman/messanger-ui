<template>
    <div style="height: 100%" class="d-flex flex-column justify-content-between flex-direction: column">
        <RightSideHeader></RightSideHeader>

        <div
                v-if="hasMessages"
                class="align-self-stretch flex-direction: column mt-auto">
            <RightSideMessagesList
                    :messages="chat.messages"></RightSideMessagesList>
        </div>
        <div v-if="!hasMessages">
            No messages
        </div>

        <RightSideInputForm
                :chat="chat"
                :messages="chat.messages"></RightSideInputForm>
    </div>
</template>

<script>
    import RightSideHeader from "./RightSideHeader";
    import RightSideMessagesList from "./RightSideMessagesList";
    import RightSideInputForm from "./RightSideInputForm";
    export default {
        name: "RightSide",
        props: [
            "chat"
        ],
        components: {RightSideInputForm, RightSideMessagesList, RightSideHeader},
        computed: {
            hasMessages() {
                let hasMessages = false;

                hasMessages = this.chat.messages != null && this.chat.messages.length > 0;

                return hasMessages;
            }
        }
    }
</script>

<style scoped>

</style>