<template>
    <div class="_1-iDe _1xXdX">
        <div class="_1FTCC">
            <HeaderSidePanel/>
            <span class="m6ZEb"></span>
            <div tabindex="-1" class="rRAIq">
                <div class="gQzdc">
                    <button class="C28xL">
                        <div v-if="this.searchParamContact == null" class="_1M3wR _3M2St">
                            <IconSearch/>
                        </div>
                        <div v-else class="_1M3wR _1BC4w"><span
                                data-icon="back-blue"
                                class=""><svg
                                xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24"><path
                                fill="currentColor"
                                d="M20 11H7.8l5.6-5.6L12 4l-8 8 8 8 1.4-1.4L7.8 13H20v-2z"></path></svg></span></div>

                    </button>
                    <span v-if="this.searchParamContact !== null">
                        <button class="_3Burg" @click="clearSearch"><span data-icon="x-alt" class=""><svg
                            xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24"><path
                            fill="currentColor"
                            d="M17.25 7.8L16.2 6.75l-4.2 4.2-4.2-4.2L6.75 7.8l4.2 4.2-4.2 4.2 1.05 1.05 4.2-4.2 4.2 4.2 1.05-1.05-4.2-4.2 4.2-4.2z"></path></svg></span></button></span>


                    <div class="_2cLHw" id="_2cLHw" style="visibility: visible;">{{searchPlaceholderContact}}</div>
                    <label class="_2MSJr">
                        <div tabindex="-1" class="_3F6QL _3xlwb">
                            <div class="_39LWd" style="visibility: visible;"></div>
                            <div id="divTextMessage"
                                 v-on:keyup.esc.exact="clearSearch"
                                 @input="handleSearchContact" class="_2S1VP copyable-text selectable-text"
                                 contenteditable="true"
                                 data-tab="3" dir="ltr"></div>
                        </div>
                    </label></div>
            </div>
            <div class="_1vDUw B5rWa" id="pane-side">
                <div tabindex="-1" data-tab="4">

                    <div class="" style="pointer-events: auto;">
                        <div class="_21sW0 _1ecJY" v-for="listChat in filteredItems" v-bind:key="listChat.chatID">
                            <!--chatchathcat-->
                            <div class="_2wP_Y"
                                 style="z-index: 46; transition: none 0s ease 0s; height: 72px;">
                                <div tabindex="-1" v-on:click="$emit('setActiveChat', listChat)">

                                    <!--style=""-->
                                    <div v-bind:class="{ '_1f1zm' : activeChat ===
                                    listChat.chatID}"
                                         class="_2EXPL">
                                        <div class="dIyEr">
                                            <div class="_1WliW" style="height: 49px; width: 49px;">
                                                <img
                                                        v-bind:src="listChat.photo"
                                                        draggable="false" class="Qgzj8 gqwaM _3FXB1"
                                                        style="visibility: visible;" alt="">

                                            </div>
                                        </div>
                                        <div class="_3j7s9">
                                            <div class="_2FBdJ">
                                                <div class="_25Ooe">
                                                            <span class="_3TEwt">
                                                            <span dir="auto" title="Una"
                                                                  class="_1wjpf _3NFp9 _3FXB1">{{listChat
                                                                .name}}</span><div
                                                                    class="_1yct0"></div></span></div>
                                                <div class="_3Bxar">{{listChat.lastChatT}}</div>
                                            </div>
                                            <div class="_1AwDx">
                                                <div class="_itDl">
                                                            <span class="_2_LEW"
                                                                  :title="listChat.lastChatM"><div
                                                                    class="_1VfKB">
                                                            <span data-icon="status-check" class="">
                                                                <svg xmlns="http://www.w3.org/2000/svg"
                                                                     viewBox="0 0 14 18"
                                                                     width="14" height="18">
                                                                <path fill="currentColor"
                                                                      d="M12.502 5.035l-.57-.444a.434.434 0 0 0-.609.076l-6.39 8.198a.38.38 0 0 1-.577.039l-2.614-2.556a.435.435 0 0 0-.614.007l-.505.516a.435.435 0 0 0 .007.614l3.887 3.8a.38.38 0 0 0 .577-.039l7.483-9.602a.435.435 0 0 0-.075-.609z"></path></svg></span></div>
                                                                <span dir="ltr"
                                                                      class="_1wjpf _3NFp9 _3FXB1">{{listChat.lastChatM}}
                                                                </span>
                                                            </span>
                                                </div>
                                                <div class="_3Bxar">
                                                            <span>
                                                                <div class="_15G96 _14MyY">
                                                                    <span data-icon="pinned" class="">
                                                                        <svg xmlns="http://www.w3.org/2000/svg"
                                                                             viewBox="0 0 19 19"
                                                                             width="19" height="19">
                                                                            <path fill="currentColor"
                                                                                  d="M9.5 18.419C4.574 18.419.581 14.426.581 9.5S4.574.581 9.5.581s8.919 3.993 8.919 8.919-3.993 8.919-8.919 8.919zm2.121-5.708l-.082-2.99 1.647-1.963a1.583 1.583 0 0 0-.188-2.232l-.32-.269a1.58 1.58 0 0 0-2.231.203L8.803 7.42l-2.964.439a.282.282 0 0 0-.14.496l5.458 4.58c.186.157.47.019.464-.224zM5.62 13.994a.504.504 0 0 0 .688-.038l2.204-2.307-1.085-.91-1.889 2.571a.504.504 0 0 0 .082.684z"></path></svg></span></div></span><span></span><span></span>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="_3lztd"></div>
            </div>
        </div>
    </div>
</template>

<script>

    import HeaderSidePanel from "@/components/SidePanelHeader";
    import IconSearch from "@/components/Icon/IconSearch";

    export default {
        name: "SidePanel",
        props: ['listChats', 'activeChat'],
        data: () => ({
            searchPlaceholderContact: 'Search or start new chat',
            searchParamContact: null
        }),
        components: {
            IconSearch,
            HeaderSidePanel
        },

        methods: {
            handleSearchContact: function (e) {
                if (e.target.textContent.length > 0) {
                    this.searchPlaceholderContact = null
                    this.searchParamContact = e.target.textContent
                } else {
                    this.searchPlaceholderContact = 'Search or start new chat'
                    this.searchParamContact = null
                }

            },
            clearSearch: function () {
                this.searchPlaceholderContact = 'Search or start new chat'
                this.searchParamContact = null
                document.getElementById("divTextMessage").textContent = ""
            }
        },
        computed: {
            filteredItems() {
                let chats = this.listChats;
                let authorNameSearchString = this.searchParamContact;
                if (!authorNameSearchString) {
                    return chats;
                }
                authorNameSearchString.trim().toLowerCase();
                return chats.filter(function (item) {
                    if (item.name.toLowerCase().indexOf(authorNameSearchString) !== -1) {
                        return item;
                    }
                });
            }
        },


    }
</script>

<style scoped>

</style>
