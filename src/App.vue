<template>
    <div id="app">
        <div class="appPraInside">
            <div tabindex="-1" class="app h70RQ two">
                <SidePanel></SidePanel>
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
        components: {
            SidePanel,
            MainPanel
        }
    }
</script>

<style>
    @import 'assets/css/style.css';
</style>
