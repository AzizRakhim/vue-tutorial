<template>
  <div>
    <div class="w-75 mx-auto">
      <h3>
        Add Comments
      </h3>
      <form @submit.prevent="createComment">
        <input 
          v-model="name"
          type="text" 
          placeholder="Enter Your Name..." 
          class="form-control"
        >
        <input 
          v-model="email"
          placeholder="Enter Your Email..." 
          class="form-control my-3"
        >
        <input 
          v-model="content"
          type="text" 
          placeholder="Enter Your Comment..." 
          class="form-control"
          >
        <div class="mt-3 d-flex flex-row-reverse">
          <button class="btn btn-primary">
            Add Comments
          </button>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name : "",
      email : "",
      content : ""
    }
  },
  methods : {
    createComment() {
      this.comment.id = Date.now();
      this.comments.push(newComment);
      this.name = "";
      this.email = "";
      this.content = "";
    }
  }
}
</script>

<style>
  
</style>