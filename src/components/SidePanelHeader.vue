<template>
    <header class="_3auIg">
        <div class="_2umId">
            <div class="_1WliW" style="height: 40px; width: 40px; cursor: pointer;">
                <img
                        src="https://picsum.photos/200"
                        draggable="false" class="Qgzj8 gqwaM _3FXB1" style="visibility: visible;" alt="">
            </div>
        </div>
        <div class="_20NlL">
            <div class="_3Kxus ba6sz">
                <div class="rAUz7">
                    <div role="button"
                         title="Status">
                        <IconStatus/>
                    </div>
                </div>
                <div class="rAUz7">
                    <div role="button" title="Chat baru">
                        <IconChat/>
                    </div>
                </div>
                <div class="rAUz7">
                    <div role="button" title="Menu">
                        <IconMenu/>
                    </div>
                </div>
            </div>
        </div>
    </header>
</template>

<script>
    import IconMenu from "@/components/Icon/IconMenu";
    import IconStatus from "@/components/Icon/IconStatus";
    import IconChat from "@/components/Icon/IconChat";

    export default {
        name: "HeaderSidePanel",
        components: {
            IconMenu,
            IconStatus,
            IconChat
        }
    }
</script>

<style scoped>

</style>
