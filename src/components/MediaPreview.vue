<template>
    <div class="_2vPAk" tabindex="-1" v-on:keyup.esc.exact="$emit('closePreview')">
        <div class="overlay JWJN5 _1zxIi  scale-in-center" data-animate-media-viewer="true">
            <div class="_3pRd1">
                <div class="_20PqB">
                    <div class="_2EXPL _1FGIr ts7je">
                        <div class="dIyEr">
                            <div class="_1WliW" style="height: 40px; width: 40px;"><img
                                    src="https://picsum.photos/id/1/200/200"
                                    draggable="false" class="Qgzj8 gqwaM _3FXB1" style="visibility: visible;">
                                <div class="_3ZW2E">
                                    <IconDefaultUser/>
                                </div>
                            </div>
                        </div>
                        <div class="_3j7s9">
                            <div class="_2FBdJ">
                                <div class="_25Ooe"><span dir="auto" class="_1wjpf _3FXB1">Anggi</span></div>
                            </div>
                            <div class="_1AwDx">
                                <div class="_itDl">today at 19:02</div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="_1_wiy">
                    <div class="_3Kxus _30525">
                        <div class="rAUz7">
                            <div role="button" title="Download">
                                <IconDownload/>
                            </div>
                            <span></span></div>
                        <div class="rAUz7">
                            <div role="button" title="Close" v-on:click="$emit('closePreview')">
                                <IconCloseX/>
                            </div>
                            <span></span></div>
                    </div>
                </div>
            </div>
            <div class="_3vXNW" dir="ltr">
                <div class="_1cVDK">
                    <div class="IuYNx _3E6Ha _2gmeM _1V8K0">
                        <div style="position: relative; width: 495.562px; height: 881px; transition: transform 300ms cubic-bezier(0.1, 0.82, 0.25, 1) 0s;">
                            <div class="rN9sv"
                                 style="opacity: 1; transform: translateX(0px) translateY(0px) scale(1);">
                                <img class="rN9sv _2-V0A _3FXB1" style="visibility: visible;"
                                     crossorigin="anonymous" :src="img" alt=""
                                     v-if="this.isImg && text.mimetype === 'image/jpeg'"/>
                                <video crossorigin="anonymous" class="rN9sv _2-V0A _3FXB1" style="visibility:
                                visible;" :src="img" autoplay
                                       controls
                                       v-else-if="this.isImg && text.mimetype === 'video/mp4'">
                                    Your browser does not support the video tag.
                                </video>
                                <p v-else>Loading...{{isImg}}</p>
                                <!-- <img
                                         crossorigin="anonymous"
                                         src="https://picsum.photos/200/600"
                                         class="rN9sv _2-V0A _3FXB1" style="visibility: visible;">-->
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import IconDefaultUser from "@/components/Icon/IconDefaultUser";
    import IconDownload from "@/components/Icon/IconDownload";
    import IconCloseX from "@/components/Icon/IconCloseX";

    export default {
        name: "MediaPreview",
        components: {
            IconCloseX, IconDownload, IconDefaultUser
        },
        props: ['text'],
        data: () => ({
            isImg: false,
            img: null
        }),
        mounted() {
            this.getImg()
            this.img = 'https://picsum.photos/id/1/200/200'
        },
        methods: {
            getImg: function () {
                this.isImg = true;
            }
        },
    }
</script>

<style scoped>

</style>
