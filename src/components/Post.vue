<template lang="html">
  <div class="post">
    <div class="upper">
      <post-body>postbody</post-body>
    </div>
    <div class="bottom">
      <comment-box>commentbox</comment-box>
    </div>
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

<style lang="css" scoped>
  .post{
    display: flex;
    flex-direction: column;
    min-height: 100vh;
  }
  .upper{
    background-color: #00bcd4;
    padding-top: 20px;
    padding-bottom: 20px;
  }
  .bottom{
    background-color: #f4f3f3;
    flex-grow: 1;
    padding-top:20px;
  }
</style>
