<template>
  <div>
    <form-helper>      
      
        <div slot="form-header">
            <h3>Form Two - Log In</h3>
            <p>Enter yout details to log-in</p>
        </div>

        <div slot="form-fields">
            <input type="text" placeholder="username" required>
            <input type="password" placeholder="password" required>
            <textarea name="" id="" cols="10" rows="5"></textarea>
        </div>

        <div id="form-controls">
            <button v-on:click="handleSubmit">Login</button>
        </div>        

    </form-helper>
  </div>
</template>

<script>
import formHelper from './formHelper.vue'

export default {
  data() {
    return {
      counter: 0
    };
  }
};
</script>

<style>