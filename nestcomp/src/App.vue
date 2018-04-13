<template>
  <div>    
    <div>
      <h1>{{title}}</h1>
      <ninja></ninja>    
    </div>
  </div>
</template>

<script>
import Ninja from "./Ninja.vue";

export default {
  components: {
    ninja: Ninja
  },
  data() {
    return {
      title: "Ninja App"
    };
  }
};
//뷰 컴포넌트를 만들어서 다른 뷰 컴포넌트안에 넣는예제를 해봤다.
//넣을때는 글로벌컴포넌트로 만들어서 줄수도 있었고, 로컬변수로 넣을 수 도있엇다.

// 컴포넌트르르 여러개 사용할때 css를 적용하는 style태그에 scoped속성을 주면
// 각각 컴포넌트에 css 속성이 적용됐다.
</script>


<style scoped>
h1 {
  color: purple;
}
</style>
