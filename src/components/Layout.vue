<template>
  <main>
    <div class="row">
      <div class="col-12 layout">
        <div class="channel-select-section px-2 py-4 justify-content-center">
          <section class="image-section py-2">
            <img
              src="../static/img/buld.jpg"
              alt=""
              height="45px"
              width="45px"
            />
          </section>
          <section class="image-section py-2">
            <img
              src="../static/img/buld.jpg"
              alt=""
              height="45px"
              width="45px"
            />
          </section>
          <section class="image-section py-2">
            <img
              src="../static/img/buld.jpg"
              alt=""
              height="45px"
              width="45px"
            />
          </section>

          <button class="floatingBtn">
            <img
              src="../static/img/plus-solid.svg"
              alt=""
              height="20px"
              width="20px"
            />
          </button>
        </div>
        <div class="channel-list-section py-4">
          <div
            class="
              currentTitle
              py-2
              px-3
              d-flex
              justify-content-between
              align-items-center
            "
          >
            <section class="d-flex align-items-center">
              <h4 class="px-2">Slack Clone</h4>
              <span>
                <img
                  src="../static/img/angle-down-solid.svg"
                  alt=""
                  height="18px"
                  width="18px"
                />
              </span>
            </section>
            <section
              class="
                plus-square
                d-flex
                justify-content-center
                align-items-center
              "
            >
              <img
                src="../static/img/plus-square-regular.svg"
                alt=""
                height="18px"
                width="18px"
              />
            </section>
          </div>

          <div class="p-2">
            <ul>
              <li class="d-flex justify-content-start align-items-center">
                <span class="px-2 tooglebtn">
                  <img
                    src="../static/img/at-solid.svg"
                    alt=""
                    height="14px"
                    width="14px"
                  />
                </span>
                <span>Mentions</span>
              </li>
              <li class="d-flex justify-content-start align-items-center">
                <span class="px-2 tooglebtn">
                  <img
                    src="../static/img/comment-dots-regular.svg"
                    alt=""
                    height="14px"
                    width="14px"
                  />
                </span>
                <span>Threads</span>
              </li>
              <li class="d-flex justify-content-start align-items-center">
                <span class="px-2 tooglebtn">
                  <img
                    src="../static/img/bell-regular.svg"
                    alt=""
                    height="14px"
                    width="14px"
                  />
                </span>
                <span>Notifications</span>
              </li>
            </ul>
          </div>

          <div class="channels p-2">
            <div class="d-flex justify-content-start align-items-center">
              <span class="tooglebtn" v-if="channelList">
                <img
                  src="../static/img/caret-right-solid.svg"
                  alt=""
                  height="18px"
                  width="18px"
                  @click="toogleChannelList()"
                />
              </span>
              <span v-else class="tooglebtn">
                <img
                  src="../static/img/caret-down-solid.svg"
                  alt=""
                  height="18px"
                  width="18px"
                  @click="toogleChannelList()"
                />
              </span>
              <h6 class="px-2">Channels</h6>
            </div>
            <ul v-if="!channelList" class="listItems">
              <li>
                <span class="px-2">#</span>
                <span>Vue gang</span>
              </li>
              <li>
                <span class="px-2">#</span>
                <span>Vue gang</span>
              </li>
              <li>
                <span class="px-2">#</span>
                <span>Vue gang</span>
              </li>
              <li>
                <span class="px-2">#</span>
                <span>Vue gang</span>
              </li>
              <li class="d-flex justify-content-start align-items-center">
                <span class="px-2 tooglebtn">
                  <img
                    src="../static/img/plus-solid.svg"
                    alt=""
                    height="15px"
                    width="15px"
                  />
                </span>
                <span>Add new Channel</span>
              </li>
            </ul>
          </div>

          <div class="direct-messages p-2">
            <div class="d-flex justify-content-start align-items-center">
              <span v-if="messageList" class="tooglebtn">
                <img
                  src="../static/img/caret-right-solid.svg"
                  alt=""
                  height="18px"
                  width="18px"
                  @click="toogleMessageList()"
                />
              </span>
              <span v-else class="tooglebtn">
                <img
                  src="../static/img/caret-down-solid.svg"
                  alt=""
                  height="18px"
                  width="18px"
                  @click="toogleMessageList()"
                />
              </span>
              <h6 class="px-2">Messages</h6>
            </div>
            <ul v-if="!messageList" class="listItems">
              <li>
                <img
                  src="../static/img/buld.jpg"
                  alt=""
                  height="30px"
                  width="30px"
                  class="ma-2 list-image"
                />
                <span>Vue gang</span>
              </li>
              <li>
                <img
                  src="../static/img/buld.jpg"
                  alt=""
                  height="30px"
                  width="30px"
                  class="ma-2 list-image"
                />
                <span>Vue gang</span>
              </li>
              <li>
                <img
                  src="../static/img/buld.jpg"
                  alt=""
                  height="30px"
                  width="30px"
                  class="ma-2 list-image"
                />
                <span>Vue gang</span>
              </li>
              <li>
                <img
                  src="../static/img/buld.jpg"
                  alt=""
                  height="30px"
                  width="30px"
                  class="ma-2 list-image"
                />
                <span>Vue gang</span>
              </li>
              <li>
                <img
                  src="../static/img/buld.jpg"
                  alt=""
                  height="30px"
                  width="30px"
                  class="ma-2 list-image"
                />
                <span>Vue gang</span>
              </li>
              <li>
                <img
                  src="../static/img/buld.jpg"
                  alt=""
                  height="30px"
                  width="30px"
                  class="ma-2 list-image"
                />
                <span>Vue gang</span>
              </li>
              <li>
                <img
                  src="../static/img/buld.jpg"
                  alt=""
                  height="30px"
                  width="30px"
                  class="ma-2 list-image"
                />
                <span>Vue gang</span>
              </li>
              <li>
                <img
                  src="../static/img/buld.jpg"
                  alt=""
                  height="30px"
                  width="30px"
                  class="ma-2 list-image"
                />
                <span>Vue gang</span>
              </li>
              <li class="d-flex justify-content-start align-items-center">
                <span class="px-2 tooglebtn">
                  <img
                    src="../static/img/plus-solid.svg"
                    alt=""
                    height="15px"
                    width="15px"
                  />
                </span>
                <span>Start Conversation</span>
              </li>
            </ul>
          </div>
        </div>
        <!-- Messageinbox -->
        <div class="messageInbox">
          <h1>message section</h1>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Temporibus
            sint amet molestias esse voluptas consequatur magni nostrum
            voluptatem voluptate soluta?
          </p>
          <HeaderSearch />
        </div>
      </div>
    </div>
  </main>
</template>
<script>
import HeaderSearch from "./HeaderSearch.vue";
export default {
  components: {
    HeaderSearch,
  },
  data() {
    return {
      channelList: false,
      messageList: false,
    };
  },
  computed: {},

  methods: {
    toogleChannelList() {
      this.channelList = !this.channelList;
    },

    toogleMessageList() {
      this.messageList = !this.messageList;
    },
  },
  mounted: function () {},
};
</script>
<style scoped>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

li {
  list-style: none;
}
.section-name {
  display: flex;
  align-items: center;
}

.tooglebtn {
  height: 25px;
  width: 25px;
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
  border-radius: 10px;
}
.tooglebtn:hover {
  background: rgb(116, 107, 107);
}

.layout {
  display: grid;
  grid-template-columns: 5% 20% 75%;
  max-height: 100vh;
  max-width: 100%;
  overflow-x: hidden;
  overflow-y: hidden;
  border-top: 0.1px solid #591e5a;
}

.channel-list-section {
  height: 100vh;
  overflow: scroll;
  overflow-x: hidden;
  overflow-y: scroll;
  background: #4a154b;
  color: white;
}
.channel-select-section {
  background: #4a154b;
  color: white;
  border-right: 0.1px solid #591e5a;
}
.messageInbox {
  height: 100vh;
}
.listItems {
  padding-left: 25px;
}
.list-image {
  border-radius: 100%;
  padding: 5px;
}
li {
  padding: 5px 0;
}

li:hover {
  background: #370338;
}
.image-section img {
  border: 3px solid #ddd;
  border-radius: 10px;
}
.floatingBtn {
  padding: 10px;
  border-radius: 100%;
  background: #a5a3a3;
  border: none;
}

.currentTitle {
  border-bottom: 0.1px solid #591e5a;
}
.plus-square {
  background: #fff;
  height: 25px;
  width: 25px;
  border-radius: 100%;
}
/* customised scroll bar code  */
/* width */
::-webkit-scrollbar {
  width: 3px;
}

/* Track */
::-webkit-scrollbar-track {
  background: #f1f1f1;
}

/* Handle */
::-webkit-scrollbar-thumb {
  background: #4a154b;
  border-radius: 10px;
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: #370338;
}
</style>
