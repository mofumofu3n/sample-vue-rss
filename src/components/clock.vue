<template>
  <div class="clock">
      <h1>{{ time }}</h1>
  </div>
</template>

<script>
    export default {
        data () {
            return { time: "00:00:00" }
        },
        mounted () {
            this.startTime()
        },
        methods: {
            startTime () {
                var today = new Date();
                var h = today.getHours();
                var m = today.getMinutes();
                var s = today.getSeconds();
                h = this.fillTime(h);
                m = this.fillTime(m);
                s = this.fillTime(s);

                this.time = h + ":" + m + ":" + s;
                var t = setTimeout(this.startTime, 500);
            },
            fillTime (i) {
                if (i < 10) { i = "0" + i};
                return i;
            }
        }
    }
</script>

<style>
</style>