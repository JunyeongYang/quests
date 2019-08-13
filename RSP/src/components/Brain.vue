<template>
  <div>
    <div class="cheat">
      도전자는... <span class="challenger">{{ cheatResult }}</span>
    </div>
    <div class="then">
      그렇다면... 
      <thumb-index 
        class="fingers"
      />
      <other-fingers 
        class="fingers"
      />
      <span class="result">
        결과값
      </span>
    </div>
  </div>
</template>

<script>
import ThumbIndex from './ThumbIndex.vue'
import OtherFingers from './OtherFingers.vue'
export default {
  name: 'Brain',
  components: {
    ThumbIndex,
    OtherFingers
  },
  data() {
    return {
      RSP: ['가위', '바위', '보'],
      cheatResult: ''
    }
  },
  mounted() {
    this.cheatResult = this.cheated()
  },
  methods: {
    cheated() {
      const cheatIndex = Math.floor(Math.random() * 3)
      return this.RSP[cheatIndex]
    }
  }
}
</script>

<style>
  .challenger {
    font-size: 1.2em;
  }
  .fingers {
    color: gray;
    opacity: 0.8;
  }
  .result {
    color: red;
    font-size: 1.2em;
  }
</style>