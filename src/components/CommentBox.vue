<template lang="html">
  <div class="comment-box">
    <div class="comment-form">
      <input type="text" name="" id="commentForm" @keyup.enter="submitComment" value="">
    </div>
    <ul>
      <li v-for="comment in comments">{{comment.text}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name:'comment-box',
  data(){
    return{
      comments:[
        {text:'这是第一条'},
        {text:'这是第二条'}
      ]
    }
  },
  methods:{
    submitComment(){
      let input = document.getElementById('commentForm');
      if (input.value !== '') {
        this.comments.push({text:input.value})
        input.value = '';
      }
    }
  }
}
</script>

<style lang="css">
.comment-box{
  min-height:150px;
  width:80%;
  margin:0 auto;
  background-color: #fff;
  box-shadow: 0 2px 2px rgba(0, 0, 0, 0.5);
  text-align: center;
  color: rgba(0, 0, 0, 0.8);
  padding: 10px;
}
li{
  list-style: none;
  line-height: 30px;

}
</style>
