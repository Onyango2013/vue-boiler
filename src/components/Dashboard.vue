<template>
	<div id="dashboard">
		<h2> Dashboard</h2>

		<div class="fixed-action-btn">
			<router-link to ="/new" class="btn-floating btn-large red" > 
				<i class="fa fa-plus"> </i>
			</router-link>
		</div>		
	</div>

</template>
<script type="text/javascript">

	import db from './firebaseInit'
	
	export default {
		name: 'dashboard',
		data() {
			return{
				employees: []

			}

		},
		created(){
			db.collection ('employees').get().then
			(querySnapshot => {
				querySnapshot.forEach( doc => {
					console.log("I am me");
					const data = {

					}
				})
			})
				
		}
	}
</script>