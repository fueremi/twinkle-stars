<template>
  <q-page class="wrapper-dashboard">
    <div class="title">Attendance</div>
    <div class="wrapper-box">
      <div class="title">Class</div>
      <div class="value">: A - Regular</div>
      <div class="title">Date</div>
      <div class="date">
        :
        {{
          currentTime.toLocaleString("en-EN", {
            weekday: "long",
            day: "numeric",
            month: "long",
            year: "numeric",
          })
        }}
      </div>
      <div class="title">Time</div>
      <div class="clock">
        : {{ currentTime.toLocaleTimeString("en-EN", { hour12: false }) }} WIB
      </div>
    </div>
    <div class="title">Not Yet</div>
    <div class="wrapper-box">
      <div class="card-student">
        <div class="left"><img src="~assets/man.png" /></div>
        <div class="right">
          <div>Rian Oktio Mersa Putra</div>
          <div>5 Years Old</div>
          <div>Not Yet</div>
        </div>
        <button>Present</button>
      </div>
      <div class="card-student">
        <div class="left"><img src="~assets/woman.png" /></div>
        <div class="right">
          <div>Juang Sabit</div>
          <div>4 Years Old</div>
          <div>Not Yet</div>
        </div>
        <button>Present</button>
      </div>
      <div class="card-student">
        <div class="left"><img src="~assets/man.png" /></div>
        <div class="right">
          <div>Hendri Antoni</div>
          <div>7 Years Old</div>
          <div>Not Yet</div>
        </div>
        <button>Present</button>
      </div>
    </div>
    <div class="title">Present</div>
    <div class="wrapper-box">
      <div class="card-student">
        <div class="left"><img src="~assets/man.png" /></div>
        <div class="right">
          <div>James Christianto</div>
          <div>5 Years Old</div>
          <div>Not Yet</div>
        </div>
        <button>Done</button>
      </div>
    </div>
    <q-btn color="purple-6" class="full-width" label="Submit" />
  </q-page>
</template>

<script setup>
import { defineComponent } from "vue";
import { useCurrentTime } from "../composables/useCurrentTime";
name: "Attendance";

const { currentTime } = useCurrentTime();
</script>

<style lang="scss" scoped>
.wrapper-dashboard {
  width: 90%;
  margin: 24px auto;
  .wrapper-box {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    width: 100%;
    background: white;
    margin: 8px auto 24px;
    border-radius: 12px;
    box-shadow: rgba(0, 0, 0, 0.1) 0px 10px 50px;
    padding: 12px 24px;
    .title {
      width: 25%;
      font-size: 16px;
    }
    .value,
    .date,
    .clock {
      width: 75%;
      font-size: 16px;
      margin: 4px 0;
    }
    .card-student {
      margin-bottom: 8px;
      display: flex;
      justify-content: space-evenly;
      align-items: center;
      width: 100%;
      gap: 8px;
      .left {
        flex: 1 1 0;
        display: flex;
        justify-content: center;
        align-items: center;
        img {
          width: 48px;
          height: 48px;
        }
      }
      .right {
        flex: 3 1 0;
        display: flex;
        flex-flow: column;
      }
      .button {
        flex: 1 1 0;
        width: 10%;
      }
    }
  }
}
</style>
