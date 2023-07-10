<template>
  <q-page>
    <div>
      <p style="font-size: 32px; text-align: center; font-weight: bold">
        Attendance
      </p>
      <div style="padding: 0 16px">
        <div @click="goback()">Back</div>

        <div style="margin-top: 12px; padding-bottom: 48px">
          <div
            style="
              text-align: center;
              font-size: 18px;
              font-weight: bold;
              margin-bottom: 16px;
            "
          >
            Today
          </div>
          <div class="flex" style="justify-content: space-between; gap: 8px">
            <div
              style="
                display: flex;
                align-item: center;
                flex-direction: row;
                gap: 8px;
              "
            >
              <q-avatar>
                <img
                  src="https://source.unsplash.com/random/200x200/?baby,boy"
                  alt="user"
                  style="width: 40px; height: 40px"
                />
              </q-avatar>
              <div style="font-size: 16px; align-items: center" class="flex">
                Rian Oktio Mersa Putra
              </div>
            </div>
            <div style="display: flex">
              <q-avatar>
                <img
                  src="~assets/unchecked.png"
                  alt="user"
                  style="width: 20px; height: 20px"
                />
              </q-avatar>
              <p class="flex" style="align-items: center; margin: 0">Hadir</p>
            </div>
          </div>

          <div class="flex" style="justify-content: space-between; gap: 8px">
            <div
              style="
                display: flex;
                align-item: center;
                flex-direction: row;
                gap: 8px;
              "
            >
              <q-avatar>
                <img
                  src="https://source.unsplash.com/random/200x200/?child,boy"
                  alt="user"
                  style="width: 40px; height: 40px"
                />
              </q-avatar>
              <div style="font-size: 16px; align-items: center" class="flex">
                John Doe
              </div>
            </div>
            <div style="display: flex">
              <q-avatar>
                <img
                  src="~assets/checked.png"
                  alt="user"
                  style="width: 20px; height: 20px"
                />
              </q-avatar>
              <p class="flex" style="align-items: center; margin: 0">Hadir</p>
            </div>
          </div>

          <div class="flex" style="justify-content: space-between; gap: 8px">
            <div
              style="
                display: flex;
                align-item: center;
                flex-direction: row;
                gap: 8px;
              "
            >
              <q-avatar>
                <img
                  src="https://source.unsplash.com/random/200x200/?child,girl"
                  alt="user"
                  style="width: 40px; height: 40px"
                />
              </q-avatar>
              <div style="font-size: 16px; align-items: center" class="flex">
                Arisa Putri
              </div>
            </div>
            <div style="display: flex">
              <q-avatar>
                <img
                  src="~assets/checked.png"
                  alt="user"
                  style="width: 20px; height: 20px"
                />
              </q-avatar>
              <p class="flex" style="align-items: center; margin: 0">Hadir</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";
import { useRouter } from "vue-router";

export default defineComponent({
  name: "AttendacePage",
  setup() {
    const router = useRouter();

    const goback = () => {
      router.push("/");
    };

    return {
      goback,
    };
  },
});
</script>

<style></style>
