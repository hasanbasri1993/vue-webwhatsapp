<template>
    <footer tabindex="-1" class="_2tW_W">
        <div class="_3pkkz V42si copyable-area">
            <div class="weEq5" style="will-change: width;">
                <div data-state="closed" class="mYCYF _3svz5">
                    <emoji-picker @emoji="append" :search="searchEmoji">
                        <div
                                class="emoji-invoker"
                                slot="emoji-invoker"
                                slot-scope="{ events: { click: clickEvent } }"
                                @click.stop="clickEvent"
                        >
                            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24">
                                <path fill="currentColor"
                                      d="M9.153 11.603c.795 0 1.439-.879 1.439-1.962s-.644-1.962-1.439-1.962-1.439.879-1.439 1.962.644 1.962 1.439 1.962zm-3.204 1.362c-.026-.307-.131 5.218 6.063 5.551 6.066-.25 6.066-5.551 6.066-5.551-6.078 1.416-12.129 0-12.129 0zm11.363 1.108s-.669 1.959-5.051 1.959c-3.505 0-5.388-1.164-5.607-1.959 0 0 5.912 1.055 10.658 0zM11.804 1.011C5.609 1.011.978 6.033.978 12.228s4.826 10.761 11.021 10.761S23.02 18.423 23.02 12.228c.001-6.195-5.021-11.217-11.216-11.217zM12 21.354c-5.273 0-9.381-3.886-9.381-9.159s3.942-9.548 9.215-9.548 9.548 4.275 9.548 9.548c-.001 5.272-4.109 9.159-9.382 9.159zm3.108-9.751c.795 0 1.439-.879 1.439-1.962s-.644-1.962-1.439-1.962-1.439.879-1.439 1.962.644 1.962 1.439 1.962z"></path>
                            </svg>
                        </div>
                        <div slot="emoji-picker" slot-scope="{ emojis, insert, display }">
                            <div class="emoji-picker"
                                 :style="{ top: display.y + 'px', left: display.x + 'px' }">
                                <div class="emoji-picker__search">
                                    <input type="text" v-model="searchEmoji" v-focus>
                                </div>
                                <div>
                                    <div v-for="(emojiGroup, category) in emojis" :key="category">
                                        <h5>{{ category }}</h5>
                                        <div class="emojis">
                <span
                        v-for="(emoji, emojiName) in emojiGroup"
                        :key="emojiName"
                        @click="insert(emoji)"
                        :title="emojiName"
                >{{ emoji }}</span>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </emoji-picker>
                </div>
            </div>
            <div tabindex="-1" class="_1Plpp">
                <div tabindex="-1" class="_3F6QL _2WovP">
                    <div v-if="this.messageDraft===''" class="_39LWd" style="visibility: visible;">Ketik pesan</div>
                    <div id="_2S1VP" class="_2S1VP copyable-text selectable-text" contenteditable="true"
                         v-on:keyup.enter.exact="clearSearch"
                         @input="typeMessage"
                         data-tab="1" dir="ltr" spellcheck="true"></div>
                </div>
            </div>
            <div class="weEq5">
                <button v-if="this.messageDraft!==''" class="_35EW6"><span data-icon="send" class=""><svg
                        xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24"
                        height="24"><path
                        fill="currentColor"
                        d="M1.101 21.757L23.8 12.028 1.101 2.3l.011 7.912 13.623 1.816-13.623 1.817-.011 7.912z"></path></svg></span>
                </button>
            </div>
        </div>
    </footer>
</template>

<script>
    import EmojiPicker from 'vue-emoji-picker'

    export default {
        name: "MainPanelFooter",
        components: {EmojiPicker},
        props: ['activeChat'],
        data() {
            return {
                searchEmoji: '',
                messageDraft: ''
            }
        },
        methods: {
            append(emoji) {
                document.getElementById("_2S1VP").textContent += emoji
                this.messageDraft += emoji
            },
            typeMessage: function (e) {
                this.messageDraft = e.target.textContent
            }
        },
        directives: {
            focus: {
                inserted(el) {
                    el.focus()
                },
            },
        },
    }
</script>

<style scoped>

</style>
