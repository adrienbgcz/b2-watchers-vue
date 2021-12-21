<template>
  <div>
    VISIBLE LIFECYCLE
    <button @click="changeObj">change obj</button>
    <button @click="changeProp">change prop</button>
  </div>
</template>

<script>
export default {
  name: "Lifecycle",
  data() {
    return {
      obj: {
        adrien: ":)",
      },
    };
  },

  methods: {
    changeObj() {
      this.obj = {
        marina: ":D",
      };
    },
    changeProp() {
      this.obj.adrien = ":(";
    },
  },

  watch: {
    obj: {
      handler(newVal, oldVal) {
        console.log("ancienne", oldVal);
        console.log("nouvelle", newVal);
      },
      deep: true,
    },
  },
};
</script>
