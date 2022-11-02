<script setup>
import { ref } from 'vue';
const input = ref(0)
let count = 0

const number = (num) => {
  count += 1
  if(count == 1) {
    input.value = ''
    input.value += num + ''
  } else {
    input.value += num + ''
  }
}

const zero = (num) => {
  if(count != 0) {
    input.value += num + ''
  }
}

const clear = () => {
  input.value = 0
  count = 0
}
let a = 0, b = 0, amal = 1

const add = () => {
  a = input.value * 1
  amal = 1
  input.value = ""
}
const minus = () => {
  a = input.value * 1
  amal = 2
  input.value = ""
}
const times = () => {
  a = input.value * 1
  amal = 3
  input.value = ""
}
const devision = () => {
  a = input.value * 1
  amal = 4
  input.value = ""
}

const result = () => {
  if(amal == 1) {
    input.value = a + input.value * 1
  } else if(amal == 2) {
    input.value = a - input.value * 1
  } else if(amal == 3) {
    input.value = a * input.value * 1
  } else if(amal == 4) {
    input.value == a / input.value * 1
  }
}

</script>

<template>
  <div class="container max-w-3xl p-3 mx-auto my-4 rounded">
    <input v-model="input" class="w-full px-2 py-4 text-3xl text-right border rounded hover:cursor-text" disabled/>
    <div>
      <div class="flex justify-between mt-2 mb-2">
        <div class="flex mr-2 text-gray-900 bg-gray-200 rounded">
          <button class="w-full py-2 cursor-pointer px-9">Rad</button>
          <span class="py-2">|</span>
          <button class="py-2 text-gray-500 cursor-pointer px-9">Deg</button>
        </div>
        <div class="flex w-24 mr-2 text-gray-900 bg-gray-200 rounded">
          <button class="w-full px-10 py-2 cursor-pointer">x!</button>
        </div>
        <div class="flex w-24 mr-2 text-gray-900 bg-gray-200 rounded">
          <button class="w-full px-10 py-2 cursor-pointer">(</button>
        </div>
        <div class="flex w-24 mr-2 text-gray-900 bg-gray-200 rounded">
          <button class="w-full px-10 py-2 cursor-pointer">)</button>
        </div>
        <div class="flex w-24 mr-2 text-gray-900 bg-gray-200 rounded">
          <button class="w-full px-10 py-2 cursor-pointer">%</button>
        </div>
        <div class="flex w-24 text-gray-900 bg-gray-200 rounded">
          <button @click="clear" class="w-full px-10 py-2 cursor-pointer">CE</button>
        </div>
      </div>
      <div class="flex justify-between mt-2 mb-2">
        <div class="flex w-24 mr-2 text-gray-900 bg-gray-200 rounded">
          <button class="w-full px-10 py-2 cursor-pointer">lnv</button>
        </div>
        <div class="flex w-24 mr-2 text-gray-900 bg-gray-200 rounded">
          <button class="w-full px-10 py-2 cursor-pointer">sin</button>
        </div>
        <div class="flex w-24 mr-2 text-gray-900 bg-gray-200 rounded">
          <button class="w-full px-10 py-2 cursor-pointer">ln</button>
        </div>
        <div class="flex w-24 mr-2 text-gray-900 bg-gray-200 rounded">
          <button @click="number(7)" class="w-full px-10 py-2 cursor-pointer">7</button>
        </div>
        <div class="flex w-24 mr-2 text-gray-900 bg-gray-200 rounded">
          <button @click="number(8)" class="w-full px-10 py-2 cursor-pointer">8</button>
        </div>
        <div class="flex w-24 mr-2 text-gray-900 bg-gray-200 rounded">
          <button @click="number(9)" class="w-full px-10 py-2 cursor-pointer">9</button>
        </div>
        <div class="flex w-24 text-gray-900 bg-gray-200 rounded">
          <button class="w-full px-10 py-2 cursor-pointer">÷</button>
        </div>
      </div>
      <div class="flex justify-between mt-2 mb-2">
        <div class="flex w-24 mr-2 text-gray-900 bg-gray-200 rounded">
          <button class="w-full px-10 py-2 cursor-pointer">π</button>
        </div>
        <div class="flex w-24 mr-2 text-gray-900 bg-gray-200 rounded">
          <button class="w-full px-10 py-2 cursor-pointer">cos</button>
        </div>
        <div class="flex w-24 mr-2 text-gray-900 bg-gray-200 rounded">
          <button class="w-full px-10 py-2 cursor-pointer">log</button>
        </div>
        <div class="flex w-24 mr-2 text-gray-900 bg-gray-200 rounded">
          <button @click="number(4)" class="w-full px-10 py-2 cursor-pointer">4</button>
        </div>
        <div class="flex w-24 mr-2 text-gray-900 bg-gray-200 rounded">
          <button @click="number(5)" class="w-full px-10 py-2 cursor-pointer">5</button>
        </div>
        <div class="flex w-24 mr-2 text-gray-900 bg-gray-200 rounded">
          <button @click="number(6)" class="w-full px-10 py-2 cursor-pointer">6</button>
        </div>
        <div class="flex w-24 text-gray-900 bg-gray-200 rounded">
          <button class="w-full px-10 py-2 cursor-pointer">x</button>
        </div>
      </div>
      <div class="flex justify-between mt-2 mb-2">
        <div class="flex w-24 mr-2 text-gray-900 bg-gray-200 rounded">
          <button class="w-full px-10 py-2 cursor-pointer">e</button>
        </div>
        <div class="flex w-24 mr-2 text-gray-900 bg-gray-200 rounded">
          <button class="w-full px-10 py-2 cursor-pointer">tan</button>
        </div>
        <div class="flex w-24 mr-2 text-gray-900 bg-gray-200 rounded">
          <button class="w-full px-10 py-2 cursor-pointer">√</button>
        </div>
        <div class="flex w-24 mr-2 text-gray-900 bg-gray-200 rounded">
          <button @click="number(1)" class="w-full px-10 py-2 cursor-pointer">1</button>
        </div>
        <div class="flex w-24 mr-2 text-gray-900 bg-gray-200 rounded">
          <button @click="number(2)" class="w-full px-10 py-2 cursor-pointer">2</button>
        </div>
        <div class="flex w-24 mr-2 text-gray-900 bg-gray-200 rounded">
          <button @click="number(3)" class="w-full px-10 py-2 cursor-pointer">3</button>
        </div>
        <div class="flex w-24 text-gray-900 bg-gray-200 rounded">
          <button class="w-full px-10 py-2 cursor-pointer">-</button>
        </div>
      </div>
      <div class="flex justify-between mt-2 mb-2">
        <div class="flex w-24 mr-2 text-gray-900 bg-gray-200 rounded">
          <button class="w-full px-10 py-2 cursor-pointer">Ans</button>
        </div>
        <div class="flex w-24 mr-2 text-gray-900 bg-gray-200 rounded">
          <button class="w-full px-10 py-2 cursor-pointer">EXP</button>
        </div>
        <div class="flex w-24 mr-2 text-gray-900 bg-gray-200 rounded">
          <button class="w-full px-10 py-2 cursor-pointer">x<sup>y</sup></button>
        </div>
        <div class="flex w-24 mr-2 text-gray-900 bg-gray-200 rounded">
          <button @click=zero(0) class="w-full px-10 py-2 cursor-pointer">0</button>
        </div>
        <div class="flex w-24 mr-2 text-gray-900 bg-gray-200 rounded">
          <button class="w-full px-10 py-2 cursor-pointer">.</button>
        </div>
        <div class="flex w-24 mr-2 font-bold text-white bg-blue-500 rounded">
          <button @click="result" class="w-full px-10 py-2 cursor-pointer">=</button>
        </div>
        <div class="flex w-24 text-gray-900 bg-gray-200 rounded">
          <button @click="add" class="w-full px-10 py-2 cursor-pointer">+</button>
        </div>
      </div>
    </div>
    
  </div>
</template>