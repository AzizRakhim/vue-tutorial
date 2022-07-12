<template>
  <div>
    <div class="w-75 mx-auto comment" v-for="comment in comments" v-bind:key="comment.id">
      <div>
        <b>Name: </b> {{ comment.name }}   
      </div>
      <div>
        <b>Email: </b> {{ comment.email }} 
      </div>
      <div>
        <b>Content: </b> {{ comment.content }}  
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    comments : {
      type : Array,
      required : true
    }
  }
}
</script>

<style scoped>
  .comment{
    border: 5px solid #ccc;
    padding: 10px;
    margin: 10px;
  }
</style>

