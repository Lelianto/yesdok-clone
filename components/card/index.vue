<template>
  <div class="card-shadow">
		<nuxt-link :to="{
			path: 'detail-page',
			query: {
				id: `${index}`
			}
		}"
		class="control-link"
		>
			<b-card
				:title="truncate(article.title, 45)"
				:img-src="article.photo"
				img-height="200px"
				img-alt="Image"
				img-top
				tag="article"
				class="mb-2"
			>
				<b-card-text class="text-justify pointer">
					{{truncate(article.text, 100)}}
				</b-card-text>
				<b-card-text>
					<b-container fluid="xs">
						<b-row>
							<b-col cols="6">
								<span class="theme-control">{{article.type}}</span>
							</b-col>
							<b-col cols="6">
								<span class="date-control">
									<b-img class="clock-control" src="@/assets/clock-regular.svg"></b-img>
									{{article.date}}
								</span>
							</b-col>
						</b-row>
					</b-container>
				</b-card-text>
			</b-card>
		</nuxt-link>
	</div>
</template>
<script>
  export default {
		props:["article", "index"],
		methods: {
			truncate(string, value) {
				return (string || '').substring(0, value) + '…';
			}
		}
  }
</script>

<style scoped>
	.clock-control {
		width: 10%;
		color: white;
		position: relative;
    top: -2px;
	}
	.theme-control {
		border: 1px solid deepskyblue;
    padding: 5px;
    border-radius: 10px;
    font-size: 12px;
    color: black;
    font-weight: 600;
		cursor: pointer;
	}
	.pointer {
		cursor: pointer;
	}
	.theme-control:hover {
		background-color: rgb(157, 228, 252);
    padding: 5px;
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
	}
	.date-control:hover {
		background-color: rgb(248, 199, 107);
    font-size: 12px;
    padding: 5px;
    color: black;
    font-weight: 600;
    border-radius: 10px;
		cursor: pointer;
	}
	.card-title {
		cursor: pointer;
    margin-bottom: 0;
    height: 100px;
    overflow: hidden;
	}
	.card-shadow {
		margin-top: 5px;
		-webkit-box-shadow: 0px 2px 5px 1px rgba(0,0,0,0.25);
		-moz-box-shadow: 0px 2px 5px 1px rgba(0,0,0,0.25);
		box-shadow: 0px 2px 5px 1px rgba(0,0,0,0.25);
	}
	.card-shadow:hover {
		margin-top: 5px;
		-webkit-box-shadow: 0px 5px 10px 1px rgba(0,0,0,0.25);
		-moz-box-shadow: 0px 5px 10px 1px rgba(0,0,0,0.25);
		box-shadow: 0px 5px 10px 1px rgba(0,0,0,0.25);
	}
	.control-link {
    text-decoration: none;
    color: black;
	}
</style>