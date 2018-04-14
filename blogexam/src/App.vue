<template>
  <div>
    <!-- <addBlog></addBlog> -->
    <show-blog></show-blog>
    <list-Blogs></list-Blogs>
  </div>
</template>

<script>
import addBlog from './components/addBlog.vue';
import showBlog from './components/showBlog.vue';
import listBlogs from './components/listBlogs.vue';

export default {  
  components: {
    'addBlog': addBlog,
    'show-blog': showBlog,
    'list-Blogs': listBlogs
  },
  data () {
    return {
      
    }
  }
}
// v-model.lazy 키워드를 알아보았다.
// 글을쓰는즉시 twoway로 반영되지는 않지만 이벤트가 발생시 바로 바뀌는 것을 볼 수 있었다.

// 체크박스를 v-model data의 배열에 넣으면 클릭시 배열에 추가가됀다.
// 추가후 배열을 v-for 돌려서 빼내는 예제를 해봤다.

//vue 파일에서 v-for오류가 나서 :key를 명시해줘야한다.

//select option 에서 data binding은 select에 v-model로 담길 배열을 선택하고
//option 을 v-for로 돌리면 선택시 나오는것을 배열에 바인드 할 수 있다

//HTTP Requests jquert의 fetch api 를 생각? 아니다 npm install vue-resource를 해서 받아야한다.
//this.$http.post를 이용하여 값을 요청하고 response를 받을수 있고 콜백을 처리할 수도 있다.

// <show-blog>에서 http get 리퀘스트로 가져와서 v-for 로 뿌려주는 예제를 해봤다. vue-rosource의 역할은 대단한것 같다.

//custom태그 에는 두가지 방법이 있다. 메인에 작성한다.
//하나는 값을 지정하지않고 그냥 v-rainbow 식으로 써서 커스텀태그를 만드느것이고,
//두번재느 값을 지정해 v-theme ="'wide'" 이런식으로 쓰는것이다. 주의할 점은
//에서 = "  ''  "  작은따옴표를 넣어줘야한다.
//v-theme:column 은 arg로 받을 수 있다.

//필터는 메인에 작성한다.
//메인에 필터를 작성한후 필터를 이용할 템플릿태그를  찾아가 | 를 붙혀주고 filter를 명시해 사용한다.

//v-model을 이용해서 글을 쓸때 data의 search에 저장하게 하고 v-for로 돌고있는 restAPI get에서 title이 search 와 일치하는것만 뿌리도록 해서
//검색 필터를 만들어 보았다.

//전역에 있던것을 로컬로 가져오는 예제이다
//필터로 설정되어있던 to-uppercase 를 지역으로 가져와서 vue에 필터를 정의하게되면
//지역으로 바뀌게 되고, 이름도 또한 바꿔줘야한다. toUppercase 
//디렉티브도 마찬가지다. 전역에 있는것을 로컬로 가져올 수 있다.

//mixin을 이해하려고 searchMixin.js를 만들었는데 이해하지 못했다..
//한페이지에서 같은 다른컴포넌트지만 겹치는게 있다면 그것을 묶어주는 기능인것 같다.
</script>

<style>
body {
  margin: 0;
  font-family: 'D2Coding';
}
</style>
