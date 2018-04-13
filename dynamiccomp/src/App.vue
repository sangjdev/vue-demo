<template>
  <div>
    <!-- <form-one></form-one>
    <form-two></form-two> -->
    <keep-alive>
      <component v-bind:is="component"></component>
    </keep-alive>    
    <button v-on:click="component = 'form-one' ">Show form one</button>
    <button v-on:click="component = 'form-two' ">Show form two</button>
  </div>
</template>

<script>
import formOne from './components/formOne.vue';
import formTwo from './components/formTwo.vue';
import formHelper from './components/formHelper.vue';

export default {  
  components: {
    'form-one': formOne,
    'form-two': formTwo,
    'formHelper': formHelper
  },
  data () {
    return {
      component: 'form-one'
    }
  }
}
// slot은 태그로 사용하게 된다면 부모 컴포넌트에 있는 요소가 오버라이딩 되지않고 slot에 들어가게 될 수 있다.
// slot을 이름으로 지정하게 된다면, 부모컴포넌트에서 지정한것을 자식태그에 주입할 수 있다.

//동적 컴포넌트상황에서 버튼으로 다른컴포넌트로 바꿀 수 있다.
//텍스트에어리어 같은 컴포넌트가 바뀌었을때 새로 초기화될 수 있는부분은 keep-alive태그를 이용해서 유지시킬 수 있다.
</script>

<style>
