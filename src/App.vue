<template>
  <n-config-provider :theme-overrides="themeOverrides">
    <n-message-provider>
      <n-notification-provider>
        <n-dialog-provider>
          <div class="main">
            <my-header/>
            <div class="content">
              <router-view/>
            </div>
            <my-footer/>
          </div>
        </n-dialog-provider>
      </n-notification-provider>
    </n-message-provider>
  </n-config-provider>
</template>
<script setup>
import {NConfigProvider} from "naive-ui";
import {RouterView} from "vue-router";
import MyHeader from "./components/MyHeader.vue";
import MyFooter from "./components/MyFooter.vue";

const themeOverrides = {
  "common": {
    "textColorBase": "#fff",
    "baseColor": "#DACCCCFF",
    "primaryColor": "#21b1ff",
    "primaryColorHover": "#62b8fc",
    "primaryColorPressed": "#7fc7fc"
  },
  "Button": {
    "textColor": "#21b1ff",
    "border": "1px solid #62b8fc",
    "borderHover": "1px solid #21b1ff",
  },
  "Collapse": {
    "titleFontSize": "18px",
    "titleTextColor": "#21b1ff",
    "arrowColor": "#21b1ff",
    "textColor": "#fff",
    "border": "1px solid #62b8fc",
    "borderHover": "1px solid #21b1ff",
  },
  "CollapseTransition": {
    "bezier": "cubic-bezier(.8,2,4)",
  }
};
</script>