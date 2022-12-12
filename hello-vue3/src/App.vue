<script setup lang="ts">
import {ref} from "vue";

const now = new Date().toLocaleTimeString();
const nowRef = ref(now);

const changeTime = () => {
  nowRef.value = new Date().toLocaleTimeString();
};

const bgColor = ref('orange');
const message = ref('クリックしてね');

const mousePointerX = ref(0);
const mousePointerY = ref(0);

// イベントオブジェクト以外を渡さない場合、呼び出し側では引数を書かなくて良い
const onMouseMove = (event: MouseEvent) => {
  mousePointerX.value = event.offsetX;
  mousePointerY.value = event.offsetY;
};

// イベントオブジェクト以外も渡す場合、$eventの指定が必要
const onClick = (event: MouseEvent, color: string) => {
  message.value = event.timeStamp.toString();
  bgColor.value = color;
};

</script>

<template>
  <div style="display: flex;">
    <div class="section1">
      <div style="width: 200px; height: 200px; background: red;" @mousemove="onMouseMove">
        カーソルを乗せてね
      </div>
      <p>x：{{ mousePointerX }} / Y：{{ mousePointerY }}</p>
    </div>
    <div class="section2">
      <div style="width: 200px; height: 200px;" :style="{background: bgColor}" @click="onClick($event, 'pink')">
        {{ message }}
      </div>
    </div>
  </div>
</template>
