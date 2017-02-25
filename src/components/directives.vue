<template lang="html">
	<div class="">
		<p v-if="display">I am true.</p>
		<p v-else="!display">I am false.</p>
		<button @click="toggle">Switch</button>
		<p>{{message}}</p>
		<p>{{computedMessage}}</p>
		<p>{{computedCount}}</p>
	</div>
</template>

<script>
export default {
	data: function() {
		return {
			display: true,
			message: 'get Rigidyrickity Wrecked',
			computedMessage: "I haven't Changed",
			count: 0
		}
	},
	methods: {
		toggle(){
			this.display = !this.display;
			this.count++;
			if(this.display){
				this.message = 'get Rigidyrickity Wrecked';
				this.count++;
			}else{
				this.message = "hi";
			}
			
		}
	},
	computed: {
		computedCount(){
			console.log('I initiated')
			if(this.count > 4){
				this.computedMessage = "I changed.";
				return 'Hi there!';
			}
		}
	}
}
	
</script>

<style lang="css">
	
</style>