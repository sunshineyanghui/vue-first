<template lang="html">
  <div class="post">
    <post-body>postbody</post-body>
    <comment-box>commentbox</comment-box>
  </div>
</template>

<script>
import PostBody from './PostBody'
import CommentBox from './CommentBox'
export default {
  name:'Post',
  components:{
    PostBody,
    CommentBox
  }
}
</script>

<style lang="css">
</style>
