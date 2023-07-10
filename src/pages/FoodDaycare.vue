<template>
  <q-page class="wrapper-dashboard">
    <div class="title">Food Daycare</div>
    <div class="wrapper-box">
      <div class="title">Class</div>
      <div class="value">: A - Regular</div>
    </div>
    <div class="title">
      {{
        currentTime.toLocaleString("en-EN", {
          weekday: "long",
          day: "numeric",
          month: "long",
          year: "numeric",
        })
      }}
    </div>
    <img
      src="~assets/makanan.webp"
      class="flex full-width q-mt-md"
      style="border-radius: 12px 12px 0 0; height: 160px; object-fit: cover"
    />
    <div class="wrapper-card">
      <div class="semi-title text-left q-mt-md">
        Rian Oktio Mersa Putra (5th)
      </div>
      <div class="paragraf">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Deserunt, illo.
        Nam, quam. Saepe accusamus molestias suscipit ducimus sapiente fugiat
        atque ab, quis maxime vero iste.
      </div>
    </div>
    <img
      src="~assets/makanan2.jpeg"
      class="flex full-width q-mt-md"
      style="border-radius: 12px 12px 0 0; height: 160px; object-fit: cover"
    />
    <div class="wrapper-card">
      <div class="semi-title text-left q-mt-md">Juang Sabit (4th)</div>
      <div class="paragraf">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Deserunt, illo.
        Nam, quam. Saepe accusamus molestias suscipit ducimus sapiente fugiat
        atque ab, quis maxime vero iste.
      </div>
    </div>
    <!-- <div class="wrapper-box">
      <input type="file" accept="image/*" capture="camera" />
    </div>
    <q-btn color="purple-6" class="full-width" label="Submit" /> -->
  </q-page>
</template>

<script setup>
import { defineComponent } from "vue";
import { useCurrentTime } from "../composables/useCurrentTime";
name: "FoodDaycare";

const { currentTime } = useCurrentTime();
</script>

<style lang="scss" scoped>
.wrapper-dashboard {
  width: 90%;
  margin: 24px auto;
  .wrapper-card {
    background: white;
    border-radius: 0 0 12px 12px;
    padding: 12px 24px;
    .semi-title {
      font-size: 16px;
      font-weight: bold;
      margin-top: 0;
    }
    .paragraf {
      margin-top: 12px;
    }
  }
  .wrapper-box {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    width: 100%;
    background: white;
    margin: 8px auto 24px;
    border-radius: 8px;
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
