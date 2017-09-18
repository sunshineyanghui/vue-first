<template lang="html">
  <div class="comment-box">
    <div class="comment-form">
      <div class="input">
        <input type="text" name="" id="commentForm" @keyup.enter="submitComment" value="">
        <div class="underline"></div>
      </div>
      <button @click="submitComment">提交</button>
    </div>
    <ul>
      <li v-for="comment in reverseComments">{{comment.text}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name:'comment-box',
  // data(){
  //   return{
  //     comments:[
  //       {text:'这是第一条'},
  //       {text:'这是第二条'}
  //     ]
  //   }
  // },
  computed:{
    comments(){
      return this.$store.state.comment.all
    },
    reverseComments(){
      return this.comments
            .slice().reverse();
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
  color: rgba(0, 0, 0, 0.8);
  padding: 10px;
}
li{
  list-style: none;
  line-height: 45px;
  font-size: 16px;

}
.comment-form{
  display: flex;
  margin-bottom: 30px;
}
.input{
  flex-grow: 1;
}
input{
  width:100%;
  height:40px;
  line-height: 40px;
  font-size: 18px;
  border:0;
  color: rgba(0, 0, 0, 0.8);
}
input:focus{
  border:0;
  outline: 0;
}
.underline{
  height:1px;
  background: #00bcd4;
}
button{
  min-width:80px;
  color:#fff;
  background-color: deeppink;
  border:0;
  margin-left:20px;
}
</style>
