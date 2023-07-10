<template>
  <q-page class="wrapper-dashboard">
    <div class="title">Menus</div>
    <div class="wrapper-menu">
      <div>
        <div class="menu" @click="pushPage('/attendance')">
          <img src="~assets/calendar.png" />
        </div>
        <p>Attendance</p>
      </div>
      <div>
        <div class="menu" @click="pushPage('/fooddaycare')">
          <img src="~assets/lunch-box.png" />
        </div>
        <p>Food Daycare</p>
      </div>
      <div>
        <div class="menu" @click="pushPage('/fooddaycare')">
          <img src="~assets/activity.png" />
        </div>
        <p>Activity</p>
      </div>
    </div>
  </q-page>
</template>

<script setup>
import { defineComponent } from "vue";
import { useRouter } from "vue-router";

name: "Dashboard";

const router = useRouter();

const pushPage = (target) => {
  router.push(target);
};
</script>

<style lang="scss" scoped>
.wrapper-dashboard {
  width: 90%;
  margin: 24px auto;
  .wrapper-box {
    display: flex;
    width: 100%;
    min-height: 320px;
    max-height: 320px;
    background: white;
    margin: 8px auto 24px;
    border-radius: 12px;
    box-shadow: rgba(0, 0, 0, 0.1) 0px 10px 50px;
    padding: 12px 24px;
  }
  .wrapper-menu {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-evenly;
    gap: 32px;
    padding: 16px;
    .menu {
      height: 80px;
      width: 80px;
      border-radius: 10px;
      background-color: white;
      box-shadow: rgba(0, 0, 0, 0.1) 0px 10px 50px;
      display: flex;
      justify-content: center;
      align-items: center;
      img {
        height: 80%;
        width: 80%;
      }
    }
    p {
      margin: 4px 0 0;
      font-weight: bold;
    }
  }
}
</style>
