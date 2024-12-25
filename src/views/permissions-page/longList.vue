<template>
	<RecycleScroller
	  class="scroller"
	  :items="list"
	  :item-size="32"
	  key-field="id"
	  v-slot="{ item }"
	>
	  <div class="user">
		{{ item.name }}
	  </div>
	</RecycleScroller>
  </template>
  
  <script>
  export default {
	data() {
    return {
      list: Array.from({ length: 200 }, (_, i) => ({ id: i + 1, name: `Item ${i + 1}` }))
    };
  }
  }
  </script>
  
  <style scoped>
  .scroller {
	height: 100%;
  }
  
  .user {
	height: 32%;
	padding: 0 12px;
	display: flex;
	align-items: center;
  }
  </style>