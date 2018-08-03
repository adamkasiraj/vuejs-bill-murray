<template>
  <div class="container-fluid py-5">
    <div class="container">
      <div class="row">
        <div class="col-12 col-lg-4">
          <div class="card bg-dark text-white mb-5">
            <div class="card-body">
              <h5 class="mb-5">Bill Murray Photo Generator</h5>

              <div class="input-group mb-5 small">
                <label for="width" class="w-100">Image Width: {{width}} px</label>
                <input v-model="width" type="range" id="width" name="width" min="100" max="1000" step="50" value="500" />
              </div>

              <div class="input-group mb-5 small">
                <label for="Height" class="w-100">Image Height: {{height}} px</label>
                <input v-model="height" type="range" id="height" name="height" min="100" max="1000" step="50" value="500" />
              </div>

            </div>
          </div>
        </div>
        <div class="col-12 col-lg-8 text-left">
          <img v-bind:src=' "https://fillmurray.com/" + width + "/" + height ' />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'FillMurray',
  data () {
    return {
      height: '500',
      width: '500'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>


input[type="range"] {
  -webkit-appearance: none;
  -webkit-tap-highlight-color: rgba(255, 255, 255, 0);
  width: 100%;
  height: 20px;
  margin: 0;
  border: none;
  padding: 1px 2px;
  border-radius: 14px;
  background: #232528;
  box-shadow: inset 0 1px 0 0 #0d0e0f, inset 0 -1px 0 0 #3a3d42;
  -webkit-box-shadow: inset 0 1px 0 0 #0d0e0f, inset 0 -1px 0 0 #3a3d42;
  outline: none; /* no focus outline */
}

input[type="range"]::-moz-range-track {
  border: inherit;
  background: transparent;
}

input[type="range"]::-ms-track {
  border: inherit;
  color: transparent; /* don't drawn vertical reference line */
  background: transparent;
}

input[type="range"]::-ms-fill-lower,
input[type="range"]::-ms-fill-upper {
  background: transparent;
}

input[type="range"]::-ms-tooltip {
  display: none;
}

/* thumb */

input[type="range"]::-webkit-slider-thumb {
  -webkit-appearance: none;
  width: 40px;
  height: 18px;
  border: none;
  border-radius: 12px;
  background-image: -webkit-gradient(linear, left top, left bottom, color-stop(0%, #529de1), color-stop(100%, #245e8f)); /* android <= 2.2 */
  background-image: -webkit-linear-gradient(top , #529de1 0, #245e8f 100%); /* older mobile safari and android > 2.2 */;
  background-image: linear-gradient(to bottom, #529de1 0, #245e8f 100%); /* W3C */
}
input[type="range"]::-moz-range-thumb {
  width: 40px;
  height: 18px;
  border: none;
  border-radius: 12px;
  background-image: linear-gradient(to bottom, #529de1 0, #245e8f 100%); /* W3C */
}

input[type="range"]::-ms-thumb {
  width: 40px;
  height: 18px;
  border-radius: 12px;
  border: 0;
  background-image: linear-gradient(to bottom, #529de1 0, #245e8f 100%); /* W3C */
}


</style>
