<template>
  <b-container fluid="xl" class="control-detail">
		<b-row class="control-row-date">
			<span class="theme-control">{{detailArticle.date}}</span>
			<span class="date-control">
				{{detailArticle.type}}
			</span>
		</b-row>
		<b-row class="control-row margin-top-title">
			<h2>{{detailArticle.title}}</h2>
		</b-row>
		<b-row class="control-row">
			<b-img class="image-control" :src="detailArticle.photo"></b-img>
		</b-row>
		<div class="margin-top"></div>
		<b-row class="control-row-article" v-for="(detail, idx) in detailArticle.text" :key="idx">
			&nbsp;&nbsp;&nbsp;&nbsp;{{detail}}
		</b-row>
  </b-container>
</template>

<script>
	import logo from '../../assets/logo-yes.png';
  export default {
		props:["detailArticle"]
  }
</script>

<style scoped>
	.theme-control {
		border: 1px solid deepskyblue;
    padding: 5px 20px;
    border-radius: 10px;
    font-size: 12px;
    color: black;
    font-weight: 600;
		cursor: pointer;
	}
	.clock-control {
		width: 10%;
		color: white;
		position: relative;
    top: -2px;
	}
	.theme-control:hover {
		background-color: rgb(157, 228, 252);
    padding: 5px 20px;
    border-radius: 10px;
    font-size: 12px;
    color: black;
    font-weight: 600;
		cursor: pointer;
	}
	.date-control {
		border: 1px solid orange;
    font-size: 12px;
    padding: 5px;
    color: black;
    font-weight: 600;
    border-radius: 10px;
		cursor: pointer;
		width: 120px;
    margin-left: 20px;
		display: flex;
    justify-content: center;
	}
	.date-control:hover {
		background-color: rgb(248, 199, 107);
    font-size: 12px;
    padding: 5px;
    color: black;
    font-weight: 600;
    border-radius: 10px;
		cursor: pointer;
		width: 120px;
    margin-left: 20px;
		display: flex;
    justify-content: center;
	}
	.control-detail {
		padding-top: 100px;
	}
	.image-control {
		margin-top: 20px;
		width: 500px;
    border-radius: 10px;
    border: 5px solid whitesmoke;
	}
	.control-row {
		margin: 0;
		display: flex;
		justify-content: center;
	}
	.control-row-article {
		margin: 0;
		text-align: justify;
		margin-bottom: 20px;
	}
	.control-row-date {
		margin: 0;
		text-align: justify;
		padding: 0px 85px;
	}
	.margin-top {
		margin-top: 50px;
	}
	.margin-top-title {
		margin-top: 15px;
		padding: 0px 70px;
	}
	@media screen and (max-width: 992px) {
		.consult {
			border: none;
			border-radius: none;
			background-color:transparent;
			font-weight: normal;
		}
		.logo-control {
    	width: 125px;
    	margin: 0px
		}
		.padding-control {
			padding: 0px;
		}
		.control-row-date {
			margin: 0;
			text-align: justify;
			padding: 0px;
		}
		.image-control {
			margin-top: 20px;
			width: 100%;
			border-radius: 10px;
			border: 5px solid whitesmoke;
		}
		.margin-top-title {
			margin-top: 15px;
			padding: 0px;
		}
		h2, .h2 {
			font-size: 1.75rem;
		}
		.date-control {
			border: 1px solid orange;
			font-size: 12px;
			padding: 5px;
			color: black;
			font-weight: 600;
			border-radius: 10px;
			cursor: pointer;
			width: 120px;
			margin-left: 10px;
			display: flex;
			justify-content: center;
		}
		.date-control:hover {
			background-color: rgb(248, 199, 107);
			font-size: 12px;
			padding: 5px;
			color: black;
			font-weight: 600;
			border-radius: 10px;
			cursor: pointer;
			width: 120px;
			margin-left: 10px;
			display: flex;
			justify-content: center;
		}
	}
</style>