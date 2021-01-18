<template>
	<div class="home">
		<h1>Home</h1>
		<pre>{{ data }}</pre>
	</div>
</template>

<script> 

import axios from 'axios';

export default {
	name: 'home', 
	data() {		
		return  {
			data: []
		}
	},
	mounted() {
		axios
		.get('https://restcountries.eu/rest/v2/name/india')
		.then(response => { 
			this.data = response.data;
		})
	}
}
</script>
