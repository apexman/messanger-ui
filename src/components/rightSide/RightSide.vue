<template>
    <div
            style="height: 100%">
        <RightSideHeader></RightSideHeader>
        <RightSideMessagesList
                :messages="chat.messages"></RightSideMessagesList>
        <RightSideInputForm
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
        components: {RightSideInputForm, RightSideMessagesList, RightSideHeader}
    }
</script>

<style scoped>

</style>