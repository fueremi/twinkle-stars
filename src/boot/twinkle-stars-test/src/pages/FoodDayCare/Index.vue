<template>
  <q-page>
    <div>
      <p style="font-size: 32px; text-align: center; font-weight: bold">
        Food Day Care
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
          <div class="flex flex-center" style="gap: 8px">
            <div style="display: flex; flex-direction: row; gap: 8px">
              <q-avatar>
                <img
                  src="https://source.unsplash.com/random/200x200/?teacher"
                  alt="user"
                />
              </q-avatar>
              <div>
                <q-img
                  src="https://source.unsplash.com/random/400x200/?food"
                  spinner-color="white"
                />
                <p>
                  Lorem ipsum dolor sit amet consectetur adipisicing elit.
                  Ullam, veniam.
                </p>
              </div>
            </div>
            <div style="display: flex; flex-direction: row; gap: 8px">
              <q-avatar>
                <img
                  src="https://source.unsplash.com/random/200x200/?mother"
                  alt="user"
                />
              </q-avatar>
              <div>
                <q-img
                  src="https://source.unsplash.com/random/400x200/?rice,food"
                  spinner-color="white"
                />
                <p>
                  Lorem ipsum dolor sit amet consectetur adipisicing elit.
                  Voluptatem, enim!
                </p>
              </div>
            </div>
          </div>

          <div
            style="
              text-align: center;
              font-size: 18px;
              font-weight: bold;
              margin-bottom: 16px;
              margin-top: 16px;
            "
          >
            11 Mei 2023
          </div>
          <div class="flex flex-center" style="gap: 8px">
            <div style="display: flex; flex-direction: row; gap: 8px">
              <q-avatar>
                <img
                  src="https://source.unsplash.com/random/200x200/?teacher"
                  alt="user"
                />
              </q-avatar>
              <div>
                <q-img
                  src="https://source.unsplash.com/random/400x200/?pizza"
                  spinner-color="white"
                />
                <p>
                  Lorem ipsum dolor sit amet consectetur adipisicing elit.
                  Ullam, veniam.
                </p>
              </div>
            </div>
            <div style="display: flex; flex-direction: row; gap: 8px">
              <q-avatar>
                <img
                  src="https://source.unsplash.com/random/200x200/?mother"
                  alt="user"
                />
              </q-avatar>
              <div>
                <q-img
                  src="https://source.unsplash.com/random/400x200/?noodle"
                  spinner-color="white"
                />
                <p>
                  Lorem ipsum dolor sit amet consectetur adipisicing elit.
                  Voluptatem, enim!
                </p>
              </div>
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
  name: "FoodDayCarePage",
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
