# Vuex 정리

## vuex란?
* 상태관리 패턴, 라이브러리
* 모든 컴포넌트들이 공유하는 상태 정보 저장소

## vuex 설치 및 등록
```
npm install vuex --save
```

* main.js
```
import Vue from 'vue'
import Vuex from 'vuex'

Vue.use(Vuex)
```

## vuex 속성 : state, getters, mutations, actions
* state: 컴포넌트 간에 공유할 data 속성/ 컴포넌트에서 사용: this.$store.state으로 접근
* getters: vue 컴포넌트에서 computed로 볼 수 있음. 특정 state에 대한 연산을 함. /컴포넌트에서 사용: this.$store.getters로 접근
* mutations: 동기적 로직. state값을 변경. method에 등록. commit을 통해 호출
* actions: 비동기적 로직. method에 등록. dispatch를 통해 호출

## vuex helpers
* vuex의 속성들을 더 쉽게 사용하는 방법
* mapState, mapGetters, mapMutations, mapActions
* 앞에 ES6 전개 연산자 ...을 사용