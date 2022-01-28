<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-title>Learn Ionic</ion-title>
      </ion-toolbar>
    </ion-header>
    
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Blank</ion-title>
        </ion-toolbar>
      </ion-header>
    
      <div id="container">
        <template v-for="( person, i ) in persons" :key="i">
			<Card :fullname="person.fullname" :account="person.account" :quote="person.quote" />
        </template>
      </div>
    </ion-content>
  </ion-page>
</template>

<script>
import { IonContent, IonHeader, IonPage, IonTitle, IonToolbar } from '@ionic/vue';
import { defineComponent } from 'vue';
import Card from '@/components/Card.vue'

export default defineComponent({
  name: "HomePage",
  components: {
    IonContent,
    IonHeader,
    IonPage,
    IonTitle,
    IonToolbar,
    Card
  },
  setup() {
  	const persons = [
  		{
  			fullname: 'sandhika Galih',
  			account: '@sandhika_galihh',
  			quote: 'Jangan lupa titik koma'
  		},
  		{
  			fullname: 'Oka Rajeb Abdillah',
  			account: '@or_abdillh',
  			quote: 'Keep calm and santuy'
  		},
  		{
  			fullname: 'Fitriana',
  			account: '@ampitz09',
  			quote: 'Be your self and never surrender'
  		}
  	];

  	return { persons }
  }
});
</script>

<style scoped>


</style>
