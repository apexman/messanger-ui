<template>
    <div style="height: 100%;">
        <table>
            <tr>
                <!--<td>Left column with users list, search, 3 lines menu, app name</td>-->
                <td class="left-side-column">
                    <LeftSide></LeftSide>
                </td>
                <!--<td>Right column with messages, place to write, search in history, 3 dots menu</td>-->
                <td class="right-side-column">
                    <RightSide :chat="chats[0]"></RightSide>
                </td>
            </tr>
        </table>
    </div>
</template>

<script>
    import Header from "./leftSide/LeftSideHeader";
    import LeftSide from "./leftSide/LeftSide";
    import RightSide from "./rightSide/RightSide";

    export default {
        name: "MainPage",
        components: {RightSide, LeftSide, Header},
        data() {
            return {
                chats: [
                    {
                        id: 1,
                        img: "",
                        messages: [
                            {
                                id: 1,
                                img: "",
                                text: "aaaaaaaaaaaaaaaa",
                                time: "",
                                isMine: false
                            },
                            {
                                id: 1,
                                img: "",
                                text: "bbbbbbbbbbbbbb",
                                time: "",
                                isMine: true
                            },
                            {
                                id: 1,
                                img: "",
                                text: "dddddddddddddffffffffa",
                                time: "",
                                isMine: false
                            },
                            {
                                id: 1,
                                img: "",
                                text: ":)",
                                time: "",
                                isMine: true
                            }
                        ]
                    }
                ]
            }
        }

    }
</script>

<style scoped>

    .left-side-column {
        width: 30%;
        vertical-align: top;
    }

    .right-side-column {
        width: 70%;
        vertical-align: top;
    }

    table, th, td {
        border: 1px solid #dee2e6;
    }

    table {
        width: 100%;
        height: 100%;
    }

</style>