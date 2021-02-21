<template>
  <div>
    <b-card
      title="Title"
      :img-src="image"
      img-alt="Image"
      img-top
      tag="article"
      style="max-width: 20rem"
      class="mb-2"
    >
      <b-card-text>
        {{ title }}
      </b-card-text>
        {{ tag }} 
      <b-button href="#" variant="primary" @click="LikeClick">Like</b-button>
      Like <b-bage variant="light" >{{like}} </b-bage>
      <b-button href="#" variant="warning" @click="LoveClick">Love</b-button>
      Love <b-bage variant="light" > {{love}} </b-bage>
    </b-card>
  </div>
</template>

<script>
export default {
  props: {
    image: String,
    title: String,
    tag: String,
  },
  data(){
      return{
          like:0,
          love:0
      };
      },
      methods: {
          LikeClick(){
              this.like++, this.$emit("callbackLike",10)
          },
          LoveClick(){
              this.love++;
              this.$emit("callbackLove",50)
          }
      }
};
</script>
