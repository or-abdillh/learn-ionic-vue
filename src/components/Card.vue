<script>
import { defineComponent } from 'vue'
import { IonCard, IonCardContent, IonCardTitle, IonCardSubtitle } from '@ionic/vue'

export default defineComponent({
	name: 'CustomCard',
	components: {
	  IonCard
	},
	props: {
		fullname: {
			type: String,
			default: 'Your fullname'
		},
		account: {
			type: String,
			default: 'Your account'
		},
		quote: {
			type: String,
			default: 'Your quote'
		},
		avatar: {
			type: String,
			default: '/assets/profile.jpg'
		}	
	},
	setup() {

		return {  }
	}
})
</script>

<template>
  <IonCard>
	<section class="card">
		<div class="card-header">
			<strong>Profile</strong>
			<small>Your personal information will be displayed here</small>
		</div>
		<div class="card-body">
			<img :src="avatar" width="100" />
			<p>{{ fullname }}</p>
			<small>{{ account }}</small>
			<small>{{ quote }}</small>
		</div>
	</section>    
  </IonCard>
</template>

<style scoped>

.card p {
	font-size: 1.35rem;
}

.card strong, .card small {
	font-size: 1.15rem;
}

.card-header, .card-body {
	padding: .75rem 1rem;;
}

.card-header, .card-body {
	display: flex;
	flex-direction: column;
	align-items: center;
	text-align: center;
}

.card-body img {
	border-radius: 50%;
	width: 45%;
}

</style>
