<template>
  <div id="wrapper">
    <div class="Text">Monaco</div>
    <div class="Editor" ref="editor"></div>
  </div>
</template>

<script>
  import * as monaco from 'monaco-editor/esm/vs/editor/editor.api'

  export default {
    name: 'landing-page',
    data () {
      return {
        editor: null
      }
    },
    model: {
      event: 'change'
    },
    mounted () {
      this.editor = monaco.editor.create(this.$refs.editor, {
        value: '',
        language: 'markdown',
        folding: true,
        foldingStrategy: 'indentation',
        automaticLayout: true,
        overviewRuleBoredr: false,
        scrollBeyondLastLine: false,
        minimap: {
          enabled: false
        }
      })
    },
    beforeDestroy () {
      this.editor && this.editor.dispose()
    }
  }
</script>

<style>
  .Text {
    padding: 0.3em;
    background: #f2f2f2;
  }

  .Editor {
    box-sizing: border-box;
    width: 100%;
    height: 10em;
    border: #f2f2f2 solid 1px;
  }
</style>

