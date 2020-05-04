<template>
    <div class="_1-iDe Wu52Z">
        <div class="_2zynu" v-if="!activeChat.chatID">
            <div class="_2IVU3">
                <div class="_2LKlu" data-asset-intro-image="true" style="transform: scale(1); opacity: 1;"></div>
                <div class="_3MiDj focus-in-contract-bck" style="opacity: 1; transform: translateY(0px);"><h1
                        class="P8cO8">Keep your phone
                    connected</h1>
                    <div class="dPZky">WhatsApp connects to your phone to sync messages. To
                        reduce data usage,
                        connect
                        your phone to Wi-Fi.
                    </div>
                    <div class="_3McX8">
                        <div class="_1TgXb"></div>
                        <div class="_2g-bt">
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="_1GX8_" id="main" v-else>
            <div class="YUoyu" data-asset-chat-background="true"></div>
            <MainPanelHeader :activeChat="activeChat"/>
            <MainPanelMessages :messages="messages" @modalImage="modalImage"/>
            <MainPanelFooter :activeChat="activeChat"/>
        </div>
    </div>
</template>

<script>

    import MainPanelFooter from "./MainPanelFooter";
    import MainPanelMessages from "./Messages";
    import MainPanelHeader from "./MainPanelHeader";

    export default {
        name: "MainPanel",
        components: {
            MainPanelHeader,
            MainPanelMessages,
            MainPanelFooter,
        },
        props: ['activeChat', 'messages'],
        methods: {
            modalImage: function (message) {
                this.$emit('modalImage', message)
            },
        }
    }
</script>

<style scoped>

</style>
