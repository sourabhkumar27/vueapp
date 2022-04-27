<template>
  <div>
    <Test @submit="onSubmit"/>
    <Parent :display_content="display_content" :display_type="display_type"/>
  </div>
</template>

<script>
import Test from "./components/test.vue"
import Parent from "./components/parent.vue"

export default {
  name: 'app',
  data() {
    return {
      display_type: "type1",
      display_content: ["Item1", "Item2", "Item3"]
    };
  },
  components: {
    Parent,
    Test
  },
  methods: {
    onSubmit(event) {
      this.display_type = event.type;
      this.display_content = event.content;
    }
  }
}
</script>

<style>
</style>
