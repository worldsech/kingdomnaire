<template>
    <div class="bg-gray-200 grid w-40 ml-130 -mt-32 justify-center h-32 rounded-xl shadow-2xl">
      <h4 class="text-green-900 font-bold">Question Tag</h4>
      <button
        :class="['bg-green-600 mb-1 text-gray-100 rounded hover:bg-green-700', { 'bg-gray-900': activeButton === 'easy' }]"
        type="button"
        @click="setActiveButton('easy')"
      >
      Easy
      </button>
  
      <button
        :class="['bg-green-600 mb-1 text-gray-100 rounded hover:bg-green-700', { 'bg-gray-800': activeButton === 'hard' }]"
        type="button"
        @click="setActiveButton('hard')"
      >
      Hard
      </button>
  
      <button
        :class="['bg-green-600 mb-1 text-gray-100 rounded hover:bg-green-700', { 'bg-gray-800': activeButton === 'extreme' }]"
        type="button"
        @click="setActiveButton('extreme')"
      >
      Extreme
      </button>
    </div>
  </template>
  
  <script>
  export default {
    name: 'QuestionTab',
    data() {
      return {
        activeButton: '', // Holds the active button value
      };
    },
    methods: {
      setActiveButton(category) {
        this.activeButton = category;
      },
    },
  };
  </script>
  