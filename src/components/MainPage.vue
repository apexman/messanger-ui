<template>
    <div style="height: 100%;">
        <b-btn style="display: none" @click="getHelloWorld">aaaaaaaaaaaaaa</b-btn>
        <table>
            <tr>
                <!--<td>Left column with users list, search, 3 lines menu, app name</td>-->
                <td class="left-side-column">
                    <LeftSide
                            v-on:onChatClick="onChatClick"
                            :chats="chats"></LeftSide>
                </td>
                <!--<td>Right column with messages, place to write, search in history, 3 dots menu</td>-->
                <td class="right-side-column">
                    <RightSide :chat="this.clickedChat"></RightSide>
                </td>
            </tr>
        </table>
    </div>
</template>

<script>
    import Header from "./leftSide/LeftSideHeader";
    import LeftSide from "./leftSide/LeftSide";
    import RightSide from "./rightSide/RightSide";
    import axios from "axios";

    export default {
        name: "MainPage",
        components: {RightSide, LeftSide, Header},
        data() {
            return {
                clickedChat: {},
                chats: [
                    {
                        id: 1,
                        img: "",
                        name: "chat1",
                        unreadMessagesCount: 15,
                        lastMessage: {
                            id: 4,
                            img: "",
                            text: ":)",
                            time: "3 days ago",
                            isMine: true
                        },
                        messages: [
                            {
                                id: 1,
                                img: "",
                                text: "aaaaaaaaaaaaaaaa",
                                time: "",
                                isMine: false
                            },
                            {
                                id: 2,
                                img: "",
                                text: "bbbbbbbbbbbbbb",
                                time: "",
                                isMine: true
                            },
                            {
                                id: 3,
                                img: "",
                                text: "dddddddddddddffffffffa",
                                time: "",
                                isMine: false
                            },
                            {
                                id: 4,
                                img: "",
                                text: ":)",
                                time: "",
                                isMine: true
                            }
                        ]
                    },
                    {
                        id: 2,
                        img: "",
                        name: "chat1",
                        unreadMessagesCount: 15,
                        lastMessage: {
                            id: 4,
                            img: "",
                            text: ":)",
                            time: "3 days ago",
                            isMine: true
                        },
                        messages: [
                            {
                                id: 1,
                                img: "",
                                text: "321423",
                                time: "",
                                isMine: false
                            },
                            {
                                id: 2,
                                img: "",
                                text: "fsadfas",
                                time: "",
                                isMine: true
                            },
                            {
                                id: 3,
                                img: "",
                                text: ";sdf;lgasd",
                                time: "",
                                isMine: false
                            },
                            {
                                id: 4,
                                img: "",
                                text: ":)",
                                time: "",
                                isMine: true
                            }
                        ]
                    },
                ]
            }
        },
        methods: {
            onChatClick(chat) {
                this.clickedChat = chat;
            },
            getHelloWorld() {
                axios
                    .get('session/increment')
                    .then(function (response) {
                        console.log(response);
                    });
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