<template>
    <header class="_2y17h">
        <div class="_3mKlI" role="button">
            <div class="_1WliW" style="height: 40px; width: 40px;"><img
                    :src="activeChat.photo"
                    class="Qgzj8 gqwaM _3FXB1" draggable="false" style="visibility: visible;">
                <div class="_3ZW2E">
                    <IconDefaultUser/>
                </div>
            </div>
        </div>
        <div class="_5SiUq" role="button">
            <div class="_16vzP">
                <div class="_3XrHh"><span class="_1wjpf _3NFp9 _3FXB1" dir="auto"
                                          title="+62 853-5341-1360">{{activeChat.name}}</span>
                </div>
            </div>
            <div class="_3sgkv Gd51Q"><span class="O90ur _3FXB1"
                                            title="terakhir dilihat kemarin pukul 07.45">terakhir dilihat kemarin pukul 07.45</span>
            </div>
        </div>
        <div class="YmSrp">
            <div class="_3Kxus ba6sz">
                <div class="rAUz7">
                    <div role="button" title="Cari...">
                        <IconSearchAlt/>
                    </div>
                    <span></span></div>
                <div class="rAUz7">
                    <div role="button" title="Lampirkan">
                        <IconClip/>
                    </div>
                    <span></span>
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
    import IconDefaultUser from "../Icon/IconDefaultUser";
    import IconSearchAlt from "../Icon/IconSearchAlt";
    import IconClip from "../Icon/IconClip";
    import IconMenu from "../Icon/IconMenu";

    export default {
        name: "MainPanelHeader",
        components: {
            IconMenu, IconClip, IconSearchAlt, IconDefaultUser
        },
        props: ['activeChat'],
    }
</script>

<style scoped>

</style>
