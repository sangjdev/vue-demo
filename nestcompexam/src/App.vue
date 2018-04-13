<template>  
  <div>
    <app-header v-bind:title="title" v-on:changeTitle="updateTitle($event)"></app-header>
    <app-ninjas v-bind:ninjas="ninjas"></app-ninjas>    
    <app-footer v-bind:title="title"></app-footer>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Ninjas from "./components/Ninjas.vue";

export default {
  components: {
    "app-header": Header,
    "app-footer": Footer,
    "app-ninjas": Ninjas
  },
  data() {
    return {
      ninjas: [
        { name: "Ryu", speciality: "Vue Components", show: false },
        { name: "Crystals", speciality: "HTML Wizardry", show: false },
        { name: "Hitori", speciality: "Click Events", show: false },
        { name: "Tango", speciality: "Conditionals", show: false },
        { name: "Kami", speciality: "Webpack", show: false },
        { name: "Yoshi", speciality: "Data Design", show: false }
      ],
      title: "Vuesss"
    };
  },
methods: {
  updateTitle : function (updatedTitle) {
    this.title = updatedTitle;
  }
}
};
// 컴포넌트폴더를 만들고 그안에 헤더 푸터  콘텐츠영역까지 넣은 후 App.vue에서 합쳤다.
// 글로벌 컴포넌트에 있는 변수를 갖다가 쓰려면 템플릿 태그에 바인드를 해주고 props 속성으로 받아야한다.
// 또한 props 속성에서 한정을 하고 싶다면 type이나 requeired속성을 이용할 수 있다.

//레퍼런스타입과  프리미티브타입
//배열을 pop했을때매 레퍼런스여서 같이다른 배열도 삭제가 되었지만
//String을 변경햇을ㄸ내느 자기자신의 props 밖에 바뀌지 않았다.

//child to parent Evnet
//$emit 과 v:on:methodName $event를 이용하면 자식에서 변경한 data를 부모에게 전달해 변경시킬수 있다.

//child에서 $emit 과 v:on:methodName $event를 통해 자식의 데이터를 부모한테 전달할 수도 있지만
//이벤트 버스를 이용할 수 있다.
//전역에서 이벤트버스를 export하고 필요한곳에서 이벤트버스를 import하고 꺼내 사용할 수 있다
</script>

<style>

</style>
