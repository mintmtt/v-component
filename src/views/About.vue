<template>
  <div class="about">
    <h1>This is an about page</h1>
    <csHello msg="Hello CS MJU" :gpa="4.0"/>
    <csForm />
  </div>
</template>

<script>
// @ is an alias to /src
import csHello from "@/components/HelloWorld.vue"; 
import csForm from "@/components/RegForm.vue";

export default {
  components: {
    csHello,
    csForm
  }
};
</script>
