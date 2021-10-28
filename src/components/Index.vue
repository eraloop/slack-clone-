<template>
  <main>
    <div
      class="
        top-header
        col-md-12
        white-text
        justify-content-between
        align-items-center
      "
    >
      <section class="col-md-10 top-header-left">
        <section
          class="arrows d-flex justify-content-between align-items-center"
        >
          <span class="px-2">
            <img
              src="../static/img/caret-left-solid.svg"
              alt=""
              height="20px"
              width="20px"
            />
          </span>
          <span class="px-2">
            <img
              src="../static/img/caret-right-solid.svg"
              alt=""
              height="20px"
              width="20px"
            />
          </span>
        </section>

        <section class="history px-2">
          <img
            src="../static/img/clock-regular.svg"
            alt=""
            height="20px"
            width="20px"
          />
        </section>
        <section class="">
          <input
            type="text"
            class="form-control inputField"
            placeholder="search"
          />
        </section>
        <section class="help px-2">
          <img
            src="../static/img/question-circle-regular.svg"
            alt=""
            height="20px"
            width="20px"
          />
        </section>
      </section>

      <!-- profile image section -->
      <section class="col-md-1 top-header-left">
        <img
          src="../static/img/buld.jpg"
          alt=""
          height="30px"
          width="30px"
          class="profileImage"
        />
      </section>
    </div>
    <Layout />
  </main>
</template>
<script>
import Layout from "./Layout.vue";
export default {
  components: {
    Layout,
  },
  data() {
    return {};
  },
  computed: {},
  methods: {},
  mounted: function () {},
};
</script>
<style scoped>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
.top-header {
  height: 50px;
  width: 100%;
  background: #4a154b;
  display: grid;
  grid-template-columns: 95% 5%;
  align-items: center;
  color: white;
}
.top-header-left,
.top-header-right {
  display: flex;
  justify-content: flex-end;
  align-items: center;
}
.profileImage {
  border-radius: 10px;
}
.inputField {
  background: #582658;
  width: 700px;
  border: none;
}
.inputField:focus {
  background: #ddd;
  outline: none;
}
</style>
