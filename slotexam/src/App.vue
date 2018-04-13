<template>
  <div>
    <form-helper>
      <!-- <h2 slot="title">{{title}}</h2>
      <p slot="text">I am the paragraph text for the slot</p> -->
      <div slot="form-header">
        <h3>This is the title of the form</h3>
        <p>Information about the form</p>        
      </div>
      <div slot="form-fields">
        <input type="text" placeholder="name" required>
        <input type="password" placeholder="password" required>
      </div>
      <div slot="form-controls">
        <button v-on:click="handleSumbit">Sumbit</button>
      </div>
    </form-helper>
  </div>
</template>

<script>
import formHelper from './components/formHelper.vue'

export default {
  components: {
    'form-helper': formHelper
  },
  data () {
    return {
      
    }
  }
}
// slot은 태그로 사용하게 된다면 부모 컴포넌트에 있는 요소가 오버라이딩 되지않고 slot에 들어가게 될 수 있다.
// slot을 이름으로 지정하게 된다면, 부모컴포넌트에서 지정한것을 자식태그에 주입할 수 있다.
</script>

<style>

</style>
