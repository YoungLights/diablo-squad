<template>
	<main>
		
		<div class="title">
			<h1>Choose your warrior</h1>
			<p>and join the squad</p>
			<button @click="toggleModal">follow your path</button>
		</div>
		
		<div class="modal" :class="{active: stateModal}">
			<div class="modal-inner">
				<div class="modal-close" @click="toggleModal">x</div>
				<h4>Your name</h4>
				<input type="text">
				<button>enter your destiny</button>
			</div>
		</div>

		<div class="squad-list">
			<div class="squad-item">
				<h4>{{name}}</h4>
				
			</div>
			
		</div>

	</main>
</template>

<script setup>
	import {ref} from 'vue'

	const stateModal = ref(false)
	const name = ref(null)

	const toggleModal = () => {
		stateModal.value = !stateModal.value
	}
</script>