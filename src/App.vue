<template>
    <div id="app">
        <div class="appPraInside">
            <div tabindex="-1" class="app h70RQ two">
                <SidePanel :listChats="listChats"></SidePanel>
                <MainPanel></MainPanel>
            </div>
        </div>
    </div>
</template>

<script>
    import SidePanel from './components/SidePanel.vue'
    import MainPanel from './components/MainPanel.vue'

    export default {
        name: 'App',
        data: () => ({
            listChats: [
                {
                    chatID: 1,
                    name: 'Una',
                    photo: 'https://picsum.photos/id/1/200/200',
                    lastChatT: '04:12',
                    lastChatM: 'lalala skksskjeje'
                },
                {
                    chatID: 2,
                    name: 'Una2',
                    photo: 'https://picsum.photos/id/31/200/200',
                    lastChatT: '04:12',
                    lastChatM: 'lalala skksskjeje'
                },
                {
                    chatID: 3,
                    name: 'Una3',
                    photo: 'https://picsum.photos/id/14/200/200',
                    lastChatT: '04:12',
                    lastChatM: 'lalala skksskjeje'
                },
                {
                    chatID: 4,
                    name: 'Una4',
                    photo: 'https://picsum.photos/id/9/200/200',
                    lastChatT: '04:12',
                    lastChatM: 'lalala skksskjeje'
                },
                {
                    chatID: 5,
                    name: 'Una5',
                    photo: 'https://picsum.photos/id/345/200/200',
                    lastChatT: '04:12',
                    lastChatM: 'lalala skksskjeje'
                },
                {
                    chatID: 6,
                    name: 'Una',
                    photo: 'https://picsum.photos/id/1/200/200',
                    lastChatT: '04:12',
                    lastChatM: 'lalala skksskjeje'
                },
                {
                    chatID: 7,
                    name: 'Una2',
                    photo: 'https://picsum.photos/id/31/200/200',
                    lastChatT: '04:12',
                    lastChatM: 'lalala skksskjeje'
                },
                {
                    chatID: 8,
                    name: 'Una3',
                    photo: 'https://picsum.photos/id/14/200/200',
                    lastChatT: '04:12',
                    lastChatM: 'lalala skksskjeje'
                },
                {
                    chatID: 9,
                    name: 'Una4',
                    photo: 'https://picsum.photos/id/9/200/200',
                    lastChatT: '04:12',
                    lastChatM: 'lalala skksskjeje'
                },
                {
                    chatID: 10,
                    name: 'Una5',
                    photo: 'https://picsum.photos/id/345/200/200',
                    lastChatT: '04:12',
                    lastChatM: 'lalala skksskjeje'
                },{
                    chatID: 11,
                    name: 'Una5',
                    photo: 'https://picsum.photos/id/345/200/200',
                    lastChatT: '04:12',
                    lastChatM: 'lalala skksskjeje'
                },
                {
                    chatID: 12,
                    name: 'Una',
                    photo: 'https://picsum.photos/id/1/200/200',
                    lastChatT: '04:12',
                    lastChatM: 'lalala skksskjeje'
                },
                {
                    chatID: 13,
                    name: 'Una2',
                    photo: 'https://picsum.photos/id/31/200/200',
                    lastChatT: '04:12',
                    lastChatM: 'lalala skksskjeje'
                },
                {
                    chatID: 14,
                    name: 'Una3',
                    photo: 'https://picsum.photos/id/14/200/200',
                    lastChatT: '04:12',
                    lastChatM: 'lalala skksskjeje'
                },
                {
                    chatID: 15,
                    name: 'Una4',
                    photo: 'https://picsum.photos/id/9/200/200',
                    lastChatT: '04:12',
                    lastChatM: 'lalala skksskjeje'
                },
                {
                    chatID: 16,
                    name: 'Una5',
                    photo: 'https://picsum.photos/id/345/200/200',
                    lastChatT: '04:12',
                    lastChatM: 'lalala skksskjeje'
                },
            ]
        }),
        components: {
            SidePanel,
            MainPanel
        }
    }
</script>

<style>
    @import 'assets/css/style.css';
</style>
