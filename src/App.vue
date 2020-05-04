<template>
    <div id="app">
        <div class="appPraInside">
            <MediaPreview v-if="activePreview" :text="previewParam" @closePreview="closePreview"/>
            <div v-else tabindex="-1" class="app h70RQ two">
                <SidePanel :listChats="listChats" :activeChat="activeChat" @setActiveChat="setActiveChat"></SidePanel>
                <MainPanel :activeChat="activeChat" :messages="messages" @modalImage="modalImage"></MainPanel>
            </div>
        </div>
    </div>
</template>

<script>
    import SidePanel from './components/SidePanel/SidePanel.vue'
    import MainPanel from './components/MainPanel/MainPanel.vue'
    import data from './models/dummy.json'
    import MediaPreview from "@/components/MediaPreview";

    export default {
        name: 'App',
        data: () => ({
            listChats: data.listChats,
            messages: data.messages.data,
            activeChat: '',
            activePreview: false,
            previewParam: null
        }),
        components: {
            MediaPreview,
            SidePanel,
            MainPanel
        }, methods: {
            setActiveChat: function (listChat) {
                this.activeChat = listChat
            },
            modalImage: function (message) {
                /*this.$modal.show(ModalImage, {
                    text: message
                }, {
                    height: 'auto',
                    width: '90%',
                    name: name,
                    resizable: true,
                    draggable: true,
                    scrollable: true
                })*/
                this.previewParam = message
                this.activePreview = true
                console.log(message)
            },
            closePreview: function () {
                this.activePreview = false
            }
        }
    }
</script>

<style>
    @import 'assets/css/var.css';
    @import 'assets/css/style.css';
</style>
