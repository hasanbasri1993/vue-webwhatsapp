<template>
    <div id="app">
        <div class="appPraInside">
            <div tabindex="-1" class="app h70RQ two">
                <SidePanel :listChats="listChats" :activeChat="activeChat" @setActiveChat="setActiveChat"></SidePanel>
                <MainPanel :activeChat="activeChat"></MainPanel>
            </div>
        </div>
    </div>
</template>

<script>
    import SidePanel from '@/components/SidePanel.vue'
    import MainPanel from '@/components/MainPanel.vue'
    import data from './models/dummy.json'

    export default {
        name: 'App',
        data: () => ({
            listChats: data.listChats,
            activeChat: ''
        }),
        components: {
            SidePanel,
            MainPanel
        }, methods: {
            setActiveChat: function (listChat) {
                this.activeChat = listChat
            }
        }
    }
</script>

<style>
    @import 'assets/css/var.css';
    @import 'assets/css/style.css';
</style>
