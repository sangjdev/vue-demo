<template>
  <div>
      <!-- <slot name="title"></slot>
      <h1>I am the form helper</h1>
      <slot name="text"></slot> -->
      <h1>plz fill out our form..</h1>
      <form>
          <div id="form-header">
            <slot name="form-header"></slot>
          </div>
          <div id="form-fields">
            <slot name="form-fields"></slot>
          </div>
          <div id="form-controls">
            <slot name="form-controls"></slot>
          </div>
          <div id="useful-links">
              <ul>
                <li><a href="#">Link 1</a></li>
                <li><a href="#">Link 2</a></li>
                <li><a href="#">Link 3</a></li>
                <li><a href="#">Link 4</a></li>             
              </ul>
          </div>
      </form>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      title: "i am a dynamic slot title"
    };
  }
};

</script>


<style scoped>
h1 {
  color: red;
}
</style>
