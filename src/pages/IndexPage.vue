<template>
	<div class="main">
		<div class="skull-btn" v-if="calaca == false">
			<h1>Click here to party</h1>
			<q-btn round @click="activateCalca()">
				<q-avatar size="250px">
				<img src="../assets/img/19654.jpg">
				</q-avatar>
			</q-btn>
		</div>
		<div v-if="calaca === true" class="skeletons">
			<img src="../assets/img/skelet.gif" alt="">
			<img src="../assets/img/skelet.gif" alt="">
			<img src="../assets/img/skelet.gif" alt="">
			<img src="../assets/img/skelet.gif" alt="">
			<img src="../assets/img/skelet.gif" alt="">
			<img src="../assets/img/skelet.gif" alt="">
			<img src="../assets/img/skelet.gif" alt="">
			<img src="../assets/img/skelet.gif" alt="">
			<img src="../assets/img/skelet.gif" alt="">
		</div>
		<div v-if="calaca === true" class="calacas">
			<img src="../assets/img/skeletons.gif" alt="">
			<video loop width=" 320" height="240" controls autoplay volume="0.45">
				<source src="../assets/vid/skull_trumpet.mp4" type="video/mp4">
			</video>
			<img src="../assets/img/skeletons.gif" alt="">
			<div class="close">
				<img src="../assets/img/bones.png" alt="bones" @click="partyPopper()">
				<p>Close</p>
			</div>
		</div>
	</div>
</template>

<script>

export default ({
	name: 'IndexPage',
	data() {
		return {
			calaca: false,
		}
	},

	methods: {
		activateCalca() {
			return this.calaca = true
		},
		partyPopper(){
			return this.calaca = false
		}
	}
})
</script>

<style lang="scss">
@font-face {
	font-family: "Pacific";
	src: url(./font/Pacifico-Regular.ttf);
}


.main {
	height: 100vh;
	width: 100vw;
	display: flex;
	flex-direction: column;
	align-items: center;
	background-color: black;

	.skull-btn {
		margin: 40px 0px 40px 0px;
		display: flex;
		align-items: center;
		flex-direction: column;

		h1 {
			color: #fff;
			font-size: 70px;
			font-weight: 100;
			font-family: "Pacific";
			margin-bottom: 50px;
			line-height: 1;
			animation: text-flicker 5s linear infinite;
			text-shadow: 2px 2px 1px rgba(0, 0, 0, .4),
				0 0 20px #fe3a80,
				0 0 40px rgba(255, 0, 91, .75),
				0 0 50px rgba(255, 0, 91, .75),
				0 0 100px rgba(255, 0, 91, .75);
		}
	}
	.skeletons{
		margin: 0;
	}
	.calacas {
		display: flex;
		align-items: center;
		video {
			width: 800px;
			height: auto;
		}
		.close{
			translate: 1px 330px;
			img{
				width: 50px;
				filter: invert(1);
			}
			p {
				color: white;
				margin-top: 10px;
				font-size: 1.3rem;
				font-family: "Pacific";
			}

		}
	}
}

</style>