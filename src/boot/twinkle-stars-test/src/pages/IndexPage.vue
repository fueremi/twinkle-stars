<template>
  <q-page>
    <!-- <h1
      style="
        text-align: center;
        font-size: 36px;
        font-weight: bold;
        margin: 0;
        height: 80px;
      "
    >
      Twinkle Star
    </h1>
    <p style="text-align: center; font-size: 16px">
      Early Childhood Education Centre
    </p>
    <div
      class="flex flex-center"
      style="gap: 4px; flex: 1 1 0; margin-top: 48px"
    >
      <div
        style="width: 120px; gap: 8px"
        class="flex flex-center"
        @click="() => pushPage('/attendance')"
      >
        <img
          src="~assets/calendar.png"
          class="shadow-3"
          style="width: 80px; height: 80px; padding: 12px; border-radius: 10px"
        />
        <p>Attendance</p>
      </div>
      <div
        style="width: 120px; gap: 8px"
        class="flex flex-center"
        @click="() => pushPage('/fooddaycare')"
      >
        <img
          src="~assets/diet.png"
          class="shadow-3"
          style="width: 80px; height: 80px; padding: 12px; border-radius: 10px"
        />
        <p>Food Daycare</p>
      </div>
      <div style="width: 120px; gap: 8px" class="flex flex-center">
        <img
          src="~assets/report.png"
          class="shadow-3"
          style="width: 80px; height: 80px; padding: 12px; border-radius: 10px"
        />
        <p>Report Activity</p>
      </div>
      <div style="width: 120px; gap: 8px" class="flex flex-center">
        <img
          src="~assets/payment.png"
          class="shadow-3"
          style="width: 80px; height: 80px; padding: 12px; border-radius: 10px"
        />
        <p>Invoice Payment</p>
      </div>
      <div style="width: 120px; gap: 8px" class="flex flex-center">
        <img
          src="~assets/ticket.png"
          class="shadow-3"
          style="width: 80px; height: 80px; padding: 12px; border-radius: 10px"
        />
        <p>Report Accident</p>
      </div>
      <div style="width: 120px; gap: 8px" class="flex flex-center">
        <img
          src="~assets/chat.png"
          class="shadow-3"
          style="width: 80px; height: 80px; padding: 12px; border-radius: 10px"
        />
        <p>Chat Real-Time</p>
      </div>
    </div> -->
  </q-page>
</template>

<script>
import { defineComponent } from "vue";
import { useRouter } from "vue-router";

export default defineComponent({
  name: "IndexPage",
  setup() {
    const router = useRouter();

    const pushPage = (target) => {
      router.push(target);
    };

    return {
      pushPage,
    };
  },
});
</script>
