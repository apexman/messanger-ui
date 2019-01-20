<template>
    <div>
        <LeftSideHeader></LeftSideHeader>
        <LeftSideChatsList></LeftSideChatsList>
    </div>
</template>

<script>
    import LeftSideHeader from "./LeftSideHeader";
    import LeftSideChatsList from "./LeftSideChatsList";
    export default {
        name: "LeftSide",
        components: {LeftSideChatsList, LeftSideHeader}
    }
</script>

<style scoped>

</style>