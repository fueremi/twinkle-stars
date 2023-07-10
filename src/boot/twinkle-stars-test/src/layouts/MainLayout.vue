<template>
  <q-layout view="lHh Lpr lFf">
    <q-page-container>
      <div class="mobile-only">
        <div class="wrapper-header">
          <h2 class="title-wrapper-layout">Attendance</h2>
          <p class="date">
            {{
              currentTime.toLocaleString("en-EN", {
                weekday: "long",
                day: "numeric",
                month: "long",
                year: "numeric",
              })
            }}
          </p>
          <p class="clock">
            {{ currentTime.toLocaleTimeString("en-EN", { hour12: false }) }}
          </p>
        </div>
        <div class="wrapper-calendar">
          <div class="calendar-box">
            <p>23</p>
            <small>June</small>
          </div>
          <div class="calendar-box">
            <p>24</p>
            <small>June</small>
          </div>
          <div class="calendar-box active">
            <p>25</p>
            <small>June</small>
          </div>
          <div class="calendar-box">
            <p>26</p>
            <small>June</small>
          </div>
          <div class="calendar-box">
            <p>27</p>
            <small>June</small>
          </div>
        </div>
        <div class="wrapper-student">
          <div class="student">
            <img
              src="~assets/profile.png"
              style="width: 48px; height: 48px; padding: 8px"
            />
            <p style="margin-top: -8px">Lionel Messi</p>
          </div>
          <div class="student">
            <img
              src="~assets/profile.png"
              style="width: 48px; height: 48px; padding: 8px"
            />
            <p style="margin-top: -8px">Lionel Messi</p>
          </div>
          <div class="student">
            <img
              src="~assets/profile.png"
              style="width: 48px; height: 48px; padding: 8px"
            />
            <p style="margin-top: -8px">Lionel Messi</p>
          </div>
          <div class="student">
            <img
              src="~assets/profile.png"
              style="width: 48px; height: 48px; padding: 8px"
            />
            <p style="margin-top: -8px">Lionel Messi</p>
          </div>
          <div class="student">
            <img
              src="~assets/profile.png"
              style="width: 48px; height: 48px; padding: 8px"
            />
            <p style="margin-top: -8px">Lionel Messi</p>
          </div>
          <div class="student">
            <img
              src="~assets/profile.png"
              style="width: 48px; height: 48px; padding: 8px"
            />
            <p style="margin-top: -8px">Lionel Messi</p>
          </div>
          <div class="student">
            <img
              src="~assets/profile.png"
              style="width: 48px; height: 48px; padding: 8px"
            />
            <p style="margin-top: -8px">Lionel Messi</p>
          </div>
          <div class="student">
            <img
              src="~assets/profile.png"
              style="width: 48px; height: 48px; padding: 8px"
            />
            <p style="margin-top: -8px">Lionel Messi</p>
          </div>
          <div class="student">
            <img
              src="~assets/profile.png"
              style="width: 48px; height: 48px; padding: 8px"
            />
            <p style="margin-top: -8px">Lionel Messi</p>
          </div>
        </div>
      </div>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from "vue";
import { useCurrentTime } from "../composables/useCurrentTime";

const linksList = [
  {
    title: "Docs",
    caption: "quasar.dev",
    icon: "school",
    link: "https://quasar.dev",
  },
  {
    title: "Github",
    caption: "github.com/quasarframework",
    icon: "code",
    link: "https://github.com/quasarframework",
  },
  {
    title: "Discord Chat Channel",
    caption: "chat.quasar.dev",
    icon: "chat",
    link: "https://chat.quasar.dev",
  },
  {
    title: "Forum",
    caption: "forum.quasar.dev",
    icon: "record_voice_over",
    link: "https://forum.quasar.dev",
  },
  {
    title: "Twitter",
    caption: "@quasarframework",
    icon: "rss_feed",
    link: "https://twitter.quasar.dev",
  },
  {
    title: "Facebook",
    caption: "@QuasarFramework",
    icon: "public",
    link: "https://facebook.quasar.dev",
  },
  {
    title: "Quasar Awesome",
    caption: "Community Quasar projects",
    icon: "favorite",
    link: "https://awesome.quasar.dev",
  },
];

export default defineComponent({
  name: "MainLayout",

  components: {},

  setup() {
    const { currentTime } = useCurrentTime();
    const leftDrawerOpen = ref(false);

    return {
      essentialLinks: linksList,
      leftDrawerOpen,
      currentTime,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },
    };
  },
});
</script>

<style scoped>
p,
small,
h1 {
  margin: 0;
}

.q-page-container {
  background: #f2f5f7;
}

.wrapper-header {
  background: #6b5cdc;
  height: 120px;
  flex-flow: column;
  display: flex;
  justify-content: center;
  align-items: center;
  padding-bottom: 16px;
  border-bottom-left-radius: 24px;
  border-bottom-right-radius: 24px;
}

.wrapper-header .title-wrapper-layout {
  margin: 0 0 24px 0;
  text-align: center;
  font-size: 28px;
  font-weight: bold;
  color: white;
}

.wrapper-header .date {
  font-size: 20px;
  font-weight: bold;
  color: white;
}

.wrapper-header .clock {
  font-size: 20px;
  font-weight: bold;
  color: white;
}

.wrapper-calendar {
  height: 64px;
  width: 90%;
  margin: -24px auto 0;
  background: white;
  border-radius: 32px;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
}

.calendar-box {
  height: 48px;
  width: 48px;
  display: flex;
  flex-flow: column;
  justify-content: center;
  align-items: center;
  font-size: 20px;
  color: #6b5cdc;
  font-weight: bold;
  line-height: 16px;
}

.calendar-box.active {
  height: 48px;
  width: 48px;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 20px;
  background: #6b5cdc;
  color: white;
  border-radius: 50%;
  font-weight: bold;
}

.wrapper-student {
  width: 90%;
  gap: 16px;
  background: white;
  margin: 12px auto;
  border-radius: 8px;
  flex-wrap: wrap;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 16px;
  font-size: 16px;
}

.student {
  display: flex;
  flex-flow: column;
  justify-items: center;
  align-items: center;
}
</style>
