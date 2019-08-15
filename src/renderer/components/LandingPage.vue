<template>
  <mark-display
    :markdown="markdown"
    @title="setTitle"
    keyboard-ctrl
    url-hash-ctrl
    auto-font-size
    auto-blank-target
  ></mark-display>
</template>

<script>
import MarkDisplay from 'vue-mark-display'

const markdown = `# Hello World
----
This is Vue Mark Display`

export default {
  components: { MarkDisplay },
  data() {
    return { markdown }
  },
  methods: {
    setTitle({ title }) {
      document.title = title
    }
  }
}
</script>

<style>
</style>
