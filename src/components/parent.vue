<template>
    <div>
      <div>
        <div :style="{color:'white', backgroundColor: color}">
          <li v-for="item in display_content" :key="item">
            {{item}}
          </li>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  props: {
    display_type: String,
    display_content: Array
  },
  data() {
    return {
    }
  },
  computed: {
    color() {
      if(this.display_type == "type1") {
        return "red";
      } else if(this.display_type == "type2") {
        return "blue";
      } else if(this.display_type == "type3") {
        return "green";
      }
    }
  },
  methods:{}
}
</script>

<style scoped>
</style>
