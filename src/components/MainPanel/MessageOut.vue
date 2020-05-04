<template>
    <div class="vW7d1 message-out focusable-list-item"
         data-id="true_6285353411360@c.us_066F4EA4EF9CD9691CB83B82FCE837CF">
        <span></span>
        <div class="_3_7SH _3DFk6 _2wOlC">
            <IconTailOut/>
            <div class="MVjBr _3e2jK">
                <div class="_2F4Rh" v-if="message.isMedia||message.isMMS">
                    <div>
                        <div class="gDOmN" style="width: 330px; height: 330px;"
                             v-on:click="$emit('modalImage', message)">
                            <img
                                    :src="'data:image/jpg;base64,'+message.body" alt="" class="_1YbLB"
                                    style="width: 100%;">
                            <div class="_1i3Za"></div>
                        </div>
                        <div class="_1uFFm">
                            <div class="_1DZAH _2Pjvv _2hrew" role="button"><span class="_3EFt_" dir="auto">{{Unix_timestamp}}</span>
                                <div class="jdhpF">
                                    <IconMsgCheck :ack="message.ack"/>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="Tkt2p" v-else>
                    <div class="copyable-text"
                         data-pre-plain-text="[01.03, 25/4/2020] Daarul Uluum Lido: ">
                        <div class="_3zb-j" dir="ltr">
                                                    <span class="_3FXB1 selectable-text invisible-space copyable-text"
                                                          dir="ltr">
                                                        <span>{{message.body}}</span>
                                                    </span>
                            <span class="ZhF0n WyHOW"></span>
                        </div>
                    </div>
                    <div class="_2f-RV">

                        <div class="_1DZAH _2hrew" role="button">
                            <span
                                    class="_3EFt_"
                                    dir="auto">{{Unix_timestamp}}</span>
                            <div class="jdhpF">
                                <IconMsgCheck :ack="message.ack"/>
                            </div>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </div>
</template>

<script>
    import IconTailOut from "../Icon/IconTailOut";
    import IconMsgCheck from "../Icon/IconMsgCheck";

    export default {
        name: "MessageOut",
        components: {
            IconMsgCheck,
            IconTailOut
        },
        props: ['message'],
        computed: {
            Unix_timestamp: function () {
                var dt = new Date(this.message.t * 1000);
                var hr = dt.getHours();
                var m = "0" + dt.getMinutes();
                //var s = "0" + dt.getSeconds();
                return hr + ':' + m.substr(-2);
            }
        }
    }
</script>

<style scoped>

</style>
