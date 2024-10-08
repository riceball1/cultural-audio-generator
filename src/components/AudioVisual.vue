<script>
export default {
  name: 'AudioVisual'
}
</script>

<template>
  <div class="main-circle">
    <div class="ring" v-for="ring in 3" :key="ring">
    </div>
  </div>
</template>

<style scoped>
.main-circle {
  width: 200px;
  height: 200px;
  border-radius: 50%;
  background-color: rgba(22, 156, 156, 0.485);
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  border: 1px solid lightgray;
  animation: vibrate 0.8s infinite;
}

.ring {
  position: absolute;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 50%;
  animation: vibrate 0.8s infinite;
}


.ring:nth-child(1) {
  width: 100px;
  height: 100px;
  background-color: rgba(22, 156, 156, 0.7);
}

.ring:nth-child(2) {
  width: 150px;
  height: 150px;
  background-color: rgba(22, 156, 156, 0.5);
}

.ring:nth-child(3) {
  width: 200px;
  height: 200px;
  background-color: rgba(22, 156, 156, 0.3);
}

.ring:nth-child(1) .inner-circle {
  width: 30px;
  height: 30px;
}

.ring:nth-child(2) .inner-circle {
  width: 40px;
  height: 40px;
}

.ring:nth-child(3) .inner-circle {
  width: 50px;
  height: 50px;
}

.ring:nth-child(1) .inner-circle:nth-child(1) { top: 10%; left: 50%; transform: translate(-50%, -50%); }
.ring:nth-child(1) .inner-circle:nth-child(2) { top: 50%; left: 10%; transform: translate(-50%, -50%); }
.ring:nth-child(1) .inner-circle:nth-child(3) { top: 50%; left: 90%; transform: translate(-50%, -50%); }
.ring:nth-child(1) .inner-circle:nth-child(4) { top: 90%; left: 50%; transform: translate(-50%, -50%); }
.ring:nth-child(1) .inner-circle:nth-child(5) { top: 30%; left: 30%; transform: translate(-50%, -50%); }
.ring:nth-child(1) .inner-circle:nth-child(6) { top: 70%; left: 70%; transform: translate(-50%, -50%); }

.ring:nth-child(2) .inner-circle:nth-child(1) { top: 20%; left: 50%; transform: translate(-50%, -50%); }
.ring:nth-child(2) .inner-circle:nth-child(2) { top: 50%; left: 20%; transform: translate(-50%, -50%); }
.ring:nth-child(2) .inner-circle:nth-child(3) { top: 50%; left: 80%; transform: translate(-50%, -50%); }
.ring:nth-child(2) .inner-circle:nth-child(4) { top: 80%; left: 50%; transform: translate(-50%, -50%); }
.ring:nth-child(2) .inner-circle:nth-child(5) { top: 40%; left: 40%; transform: translate(-50%, -50%); }
.ring:nth-child(2) .inner-circle:nth-child(6) { top: 60%; left: 60%; transform: translate(-50%, -50%); }

.ring:nth-child(3) .inner-circle:nth-child(1) { top: 30%; left: 50%; transform: translate(-50%, -50%); }
.ring:nth-child(3) .inner-circle:nth-child(2) { top: 50%; left: 30%; transform: translate(-50%, -50%); }
.ring:nth-child(3) .inner-circle:nth-child(3) { top: 50%; left: 70%; transform: translate(-50%, -50%); }
.ring:nth-child(3) .inner-circle:nth-child(4) { top: 70%; left: 50%; transform: translate(-50%, -50%); }
.ring:nth-child(3) .inner-circle:nth-child(5) { top: 50%; left: 50%; transform: translate(-50%, -50%); }
.ring:nth-child(3) .inner-circle:nth-child(6) { top: 60%; left: 60%; transform: translate(-50%, -50%); }

@keyframes vibrate {
    0% { transform: scale(1); }
    50% { transform: scale(1.1); }
    100% { transform: scale(1); }
}
</style>