<template>
  <label class="switch">
    <input type="checkbox" />
    <span class="slider round"></span>
  </label>
</template>

<script>
export default {}
</script>

<style scoped>
.switch {
  position: relative;
  display: inline-block;
  width: 26px;
  height: 16px;
}

.switch input {
  opacity: 0;
  width: 0;
  height: 0;
}

.slider {
  position: absolute;
  cursor: pointer;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: #ccc;
  -webkit-transition: 0.4s;
  transition: 0.4s;
}

.slider:before {
  position: absolute;
  content: '';
  height: 12px;
  width: 12px;
  left: 2px;
  bottom: 2px;
  background-color: white;
  -webkit-transition: 0.4s;
  transition: 0.4s;
}

input:checked + .slider {
  background-color: #5469d4;
}

input:focus + .slider {
  box-shadow: 0 0 1px #5469d4;
}

input:checked + .slider:before {
  -webkit-transform: translateX(10px);
  -ms-transform: translateX(10px);
  transform: translateX(10px);
}

/* Rounded sliders */
.slider.round {
  border-radius: 10px;
}

.slider.round:before {
  border-radius: 50%;
}
</style>
