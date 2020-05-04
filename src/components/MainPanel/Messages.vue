<template>
    <div class="_3zJZ2">
        <div class="V42si copyable-area"><span></span><span></span>
            <div class="_2nmDZ" tabindex="0">
                <div class="wml2-"></div>
                <div class="_9tCEa slide-in-bottom" tabindex="-1" v-bind:key="message.id" v-for="message in messages">
                    <MessageOut :message="message" @modalImage="modalImage" v-if="message.isMe"/>
                    <MessageIn :message="message" @modalImage="modalImage" v-else/>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import MessageIn from "./MessageIn";
    import MessageOut from "./MessageOut";

    export default {
        name: "Messages",
        components: {
            MessageOut,
            MessageIn
        },
        props: ['messages'],
        methods: {
            scrollToEnd: function () {
                const container = this.$el.querySelector("._9tCEa");
                container.scrollTop = container.scrollHeight;
            },
            modalImage: function (message) {
                this.$emit('modalImage', message)
            },
            updated() {
                this.scrollToEnd()
            },
            mounted() {
                this.scrollToEnd()
            },

        },
        computed: {

            filteredMessages() {
                let messages = messages;
                let authorNameSearchString = this.messages;
                if (!authorNameSearchString) {
                    return messages;
                }
                authorNameSearchString.trim().toLowerCase();
                return messages.filter(function (item) {
                    if (item.body.toLowerCase().indexOf(authorNameSearchString) !== -1) {
                        return item;
                    }
                });
            }
        },
    }
</script>

<style scoped>

</style>
