<template>
  <div>
    <p>
      Count: <strong>{{ count }}</strong>
    </p>
    <button class="btn btn-success" v-on:click="increment">Increment</button>
    <button class="btn btn-primary" @click="decrement">Decrement</button>

    <comment-form />
    <comment-list v-bind:comments="comments" />
  </div>
</template>

<script>
import CommentForm from "./components/CommentForm";
import CommentList from "./components/CommentList";
export default {
  components : {
    CommentForm, 
    CommentList
  },
  data() {
    return {
      message : "Hello Vue!",
      count : 0,
      comments : [
        { id : 1, name : "Samar", email : "samar@gmail.com", content : "Lorem Ipsum content" },
        { id : 2, name : "Yusuf", email : "yusuf@gmail.com", content : "Lorem Ipsum content" },
        { id : 3, name : "Yunus", email : "yunus@gmail.com", content : "Lorem Ipsum content" }
      ],
    }
  },
  methods: {
    increment(){
      this.count++;
    },
    decrement(){
      this.count--;
    }
  },
}
</script>

<style>
  *{
    margin: 0;
    padding: 0;
  }
</style>
