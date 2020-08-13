<template>
  <div>
		<b-container fluid="xs" class="footer-control">
			<b-row class="row-control-margin">
				<b-col lg="4" md="12" sm="12" xs="12">
					<div class="logo-set">
						<b-img class="footer-yes" src="@/assets/logo-yes.png"></b-img>
					</div>
					<div class="text-control">
						<strong>YesDok</strong> adalah layanan e-Health yang terjangkau dengan platform mobile yang mudah digunakan dan tangguh. Menembus 17.504 pulau dan 260 juta pengguna di Indonesia.
					</div>
					<div class="avail-control">
						Available at
					</div>
					<div class="avail-control">
						<b-img class="footer-play" src="@/assets/app-play.png">
						</b-img>
					</div>
				</b-col>
				<b-col class="res-margin" lg="4" md="6" sm="6" xs="12">
					<span class="control-address">
						<h2>
							INDONESIA
						</h2>
						<b-row>
							<b-col cols="2">
								<b-img class="control-flag" src="@/assets/indo.png"></b-img>
							</b-col>
							<b-col cols="10">		
								<strong>
									PT. Yes Dok Indonesia, 
								</strong> 
								<br>
								Ruko Kirana Boutique <br>
								Jl. Boulevard Gading Raya <br>
								Blok F3 No.11 <br>
								Jakarta 14240
							</b-col>
						</b-row>
						<h2 class="margin-control">
							SINGAPORE
						</h2>
						<b-row>
							<b-col cols="2">
								<b-img class="control-flag" src="@/assets/sing.png"></b-img>
							</b-col>
							<b-col cols="10">
								<strong>
									YesDok Pte. Ltd.
								</strong>
							</b-col>
						</b-row>
					</span>
				</b-col>
				<b-col class="res-margin" lg="4" md="6" sm="6" xs="12">
					<span class="control-email">
						<h2>
							KONTAK
						</h2>
						<b-row>
							<b-col cols="2">
								<b-img class="control-email" src="@/assets/email.png"></b-img>
							</b-col>
							<b-col cols="10">		
								<strong>
								Corporate Info : <br>
								</strong>
								info@yesdok.com
							</b-col>
						</b-row>
						<b-row>
							<b-col cols="2">
								<b-img class="control-email" src="@/assets/email.png"></b-img>
							</b-col>
							<b-col cols="10">		
								<strong>
								Customer Service : <br>
								</strong>
								help@yesdok.com
							</b-col>
						</b-row>
						<h2 class="margin-control-email">
							FOLLOW US
						</h2>
						<b-row>
							<b-col cols="2">
								<b-img class="control-icon" src="@/assets/fb.svg"></b-img>
							</b-col>
							<b-col cols="2">
								<b-img class="control-icon" src="@/assets/tw.png"></b-img>
							</b-col>
							<b-col cols="2">
								<b-img class="control-icon" src="@/assets/insta.webp"></b-img>
							</b-col>
						</b-row>
					</span>
				</b-col>
			</b-row>
		</b-container>
	</div>
</template>
<script>
  export default {
  }
</script>

<style scoped>
	.footer-control {
		background-color:#b0cac7;
		margin-top: 50px;
	}
	.footer-yes {
		width: 50%;
	}
	.footer-play {
		width: 200px;
	}
	.row-control-margin {
		margin: 0;
		padding: 55px 20px;
	}
	.logo-set {
		display: flex;
    justify-content: center;
	}
	.text-control {
		margin-top: 20px;
		text-align: center;
	}
	.avail-control {
		margin-top: 20px;
		text-align: center;
		font-weight: bold;
		font-size: 28px;
	}
	.control-app {
		display: flex;
    justify-content: center;
	}
	.control-flag {
		width: 35px;
		border-radius: 50%;
	}
	.control-email {
		width: 35px;
    position: relative;
    border-radius: 50%;
	}
	.margin-control {
    margin-top: 50px;
	}
	.control-icon {
		width: 35px;
		border-radius: 50%;
	}
	.margin-control-email {
		margin-top: 75px;
	}
	@media screen and (max-width: 992px) {
		.res-margin {
			margin-top: 50px;
		}
	}
</style>