<template>
<h1>
	Home Page
</h1>
<h2>Reentaly viewd</h2>
<h2>Work Spaces  </h2>
<input type="text" v-model="nwsp" @keyup.enter="createworkspace">
<button @click="createworkspace"> create workspace </button>
<ul>
	<li v-for="wsp in wops" :key="wsp.id">
		{{wsp.id}} -- {{wsp.name}}
	</li>
</ul>
</template>
<script setup>
import { ref } from 'vue'
const nwsp = ref('')

const createworkspace = () => {
	wops.value.push({
		id: Math.floor(Math.random() * 1000),
		name: nwsp.value
	})
	nwsp.value=''
}
const wops = ref([
	{ id: 122, name: "Test 33" },
	{ id: 150, name: "New Work space" }
	
])
</script>


