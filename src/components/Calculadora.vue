<template>
	<div id="calculadora">
		<section class="calculadora-Number"> 
			<h1>Calculadora</h1><br>
			<input type="number" v-model.number=""><br>
			<input type="number" v-model.number=""><br>
			<input type="number" v-model.number=""><br>
		</section>
		<section class="calculadora-Btn">
			<div>
				<button class="btn" v-on:click="cal('soma')">+</button>
				<button class="btn" v-on:click="cal('subtração')">-</button>
			</div>
			<br>
			<div>
				<button class="btn" v-on:click="cal('multiplicação')">*</button>
				<button class="btn" v-on:click="cal('divisão')">/</button>
			</div>	
			<br>
			<button class="btn-zerar" v-on:click="zerar">C</button>
		</section>
	</div>
</template>
<script>
	export default {
		name: 'Calculadora',
  		data () {
    return {
      msg: ''
    }
  }
}
</script>
<style scoped>
	#calculadora{
		display: flex;
		justify-content: center;
		align-items: center;
		flex-direction: column;
		min-height: 50vh;
		border: solid 2px rgba(0, 0, 0, 0.2); 
		border-radius: 15px;
		width: 55%;
		margin-top: 30%;
		margin: 23%;
		box-shadow: 1px 1px 20px #999 inset;	
	}
	h1{
		font-size: 2em;
		font-family: inherit;
		font-style: italic;
		font-weight: 900;
		padding: 20px ;
		color:rgba(0, 0, 0, 0.4);
	}
	input{
		border: solid 1px #000 ;
		border-radius: 20px;
		padding: 2px 2px;
	}
	.calculadora-Number{
		display: flex;
		justify-content: center;
		align-items: center;
		flex-direction: column;
	}
	.calculadora-Btn{
		display: flex;
		justify-content: center;
		align-items: center;
		flex-direction: column;
	}
	.btn{
		padding: 10px 15px;
		border: solid 1px #000;
		border-radius: 50%;
	}
	.btn-zerar{
		padding: 5px 60px;
		border: solid 1px #000;
		margin: 10%;
		border-radius: 10px;
	}

</style>