<template>
  <div
    class="ui vertical masthead center aligned"
    id="header"
  >
    <div id="header-content">
      <h1 class="ui inverted header">
        {{ header }}
      </h1>
    </div>
  </div>
</template>
<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "TheHeader",
  setup() {
    const { header, subHeader } = window.__PRE_CONFIG__;
    return {
      header,
      subHeader,
    };
  },
});
</script>
<style>
#header {
  height: 5rem;
  position: relative;
}

#header::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  z-index: 1;
  width: 100%;
  background: rgba(66, 64, 64, 0.15);
}

#header-content {
  position: absolute;
  z-index: 3;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-shadow: 2px 2px 2px #666;
  text-align: center;
}

#header h1 {
  font-size: 3.57rem;
  white-space: nowrap;
}

#header p {
  font-size: 1.5rem;
  color: aliceblue;
}
</style>
