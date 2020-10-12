<template>
  <div ref="viewer" />
</template>

<script>
import WebViewer from '@pdftron/webviewer';
export default {
  props: {
    url: {
      type: String,
      required: true
    }
  },

  mounted () {
    //   return;

    const instance = WebViewer({

      path: '/webviewer',
      initialDoc: 'https://pdftron.s3.amazonaws.com/downloads/pl/demo-annotated.pdf'
    }, this.$refs.viewer.$el
    );
    console.log(instance);
  }
}
</script>

<style>

</style>
