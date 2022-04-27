<template>
    <div>
      <div>
        <input type="radio" name="type" value="type1" v-model="display_type" />Type1
        <input type="radio" name="type" value="type2" v-model="display_type" />Type2
        <input type="radio" name="type" value="type3" v-model="display_type" />Type3
      </div>
      <div>
        <button @click="onClick">Submit</button>
      </div>
    </div>
</template>

<script>
export default {
  data() {
    return {
      display_type: 'type1'
    }
  },
  methods:{
    onClick() {
      this.$emit("submit", {type: this.display_type, content:[
        Math.random().toString(), Math.random().toString(), Math.random().toString()
      ]});
    }
  }
}
</script>

<style scoped>
</style>
