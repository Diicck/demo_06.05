<script setup>
import {reactive, ref} from "vue";

const person = reactive({
  name: "张三",
  age: 20,
  address:'河北软件',
  phone:1241763523,
  a:{
    b:{
      c:"123"
    }
  },
  hobby:['d','a']
})

const ChangeData = ()=>{
  person.name = "李四"
  person.age = 18
  console.log(person)
  person.address = "唐山工业"
  person.phone = 17289217373
  person.hobby[0] = "学习"

  console.log(person.a.b.c)

  person.sex = "男"
}



</script>

<template>
  <div>

<!--    <h1>嘻嘻</h1>-->
    <p>姓名: {{ person.name }}</p>
    <p>手机号: {{ person.phone }}</p>
    <p>地址: {{ person.address }}</p>
    <p>年龄: {{ person.age }}</p>
    <p>{{ person.hobby }}</p>
    <p v-if="person.sex">{{ person.sex }}</p>
    <button @click="ChangeData">ChangeValue</button>

  </div>

</template>

<style scoped>
div{
  padding: 20px;
  border-radius: 15px;
  background-color: #e6e6e6;

}

</style>
