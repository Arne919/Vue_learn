<template>
  <div>
    <h1>Todo Project</h1>
    <h2>완료된 Todo 개수 : {{ store.doneTodosCount }}</h2>
    <TodoList />
    <TodoForm />
  </div>
</template>

<script setup>
import TodoForm from '@/components/TodoForm.vue'
import TodoList from '@/components/TodoList.vue'
// 1. 중앙 저장소 가져오기
import { useCounterStore } from '@/stores/counter'

// 2. 중앙 저장소를 활용해 인스턴스 생성
const store = useCounterStore()

// 3. 중앙 저장소에 상태를 참조
// console.log(store.count)

//[주의] 각 컴포넌트에서는 중앙저장소에 새로운 상태를 생성할 수 없다.
// store.ssafy = 'ssafy'

</script>

<style scoped>

</style>