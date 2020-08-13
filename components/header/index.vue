<template>
  <div class="header-control">
		<b-navbar toggleable="lg" type="dark" variant="info">
			<b-navbar-brand >
				<nuxt-link to="/">
					<b-img class="logo-control" src='@/assets/logo-yes.png'>
					</b-img>
				</nuxt-link>
			</b-navbar-brand>
			<b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
			<b-collapse id="nav-collapse" is-nav>
				<b-navbar-nav class="ml-auto">
					<b-nav-item class="padding-control">
						<nuxt-link :to="{
							path: 'theme',
							query: {
								theme: 'diet'
							}
						}"
						class="control-link"
						>
							Diet
						</nuxt-link>
					</b-nav-item>
					<b-nav-item class="padding-control">
						<nuxt-link :to="{
							path: 'theme',
							query: {
								theme: 'gaya-hidup'
							}
						}"
						class="control-link"
						>
							Gaya Hidup
						</nuxt-link>
					</b-nav-item>
					<b-nav-item class="padding-control">
						<nuxt-link :to="{
							path: 'theme',
							query: {
								theme: 'terkini'
							}
						}"
						class="control-link"
						>
							Berita Terkini
						</nuxt-link>
					</b-nav-item>
					<b-nav-item @click="showMsgBoxTwo" class="padding-control consult">
						Konsultasi
					</b-nav-item>
					<b-nav-item-dropdown class="padding-control" right>
						<template v-slot:button-content>
							<span class="color-white">
								Tentang Kami
							</span> 
						</template>
						<b-dropdown-item>Perusahaan</b-dropdown-item>
						<b-dropdown-item>Jasa</b-dropdown-item>
						<b-dropdown-item>Hubungi Kami</b-dropdown-item>
					</b-nav-item-dropdown>
				</b-navbar-nav>
			</b-collapse>
		</b-navbar>
	</div>
</template>
<script>
	import logo from '../../assets/logo-yes.png';
  export default {
		data() {
      return {
        textBox: ''
      }
    },
		methods: {
			showMsgBoxTwo() {
        this.textBox = ''
        this.$bvModal.msgBoxOk('Selamat Anda Berhasil Berkonsultasi!', {
          title: 'Confirmation',
          size: 'sm',
          buttonSize: 'sm',
          okVariant: 'success',
          headerClass: 'p-2 border-bottom-0',
          footerClass: 'p-2 border-top-0',
          centered: true
        })
          .then(value => {
            this.textBox = value
          })
          .catch(err => {
            // An error occurred
          })
      }
		}
  }
</script>

<style scoped>
	.header-control {
		position: fixed;
    top: 0;
    right: 0;
    left: 0;
    width: 100%;
    z-index: 500;
	}
	.logo-control {
		width: 125px;
		margin: 0px 20px;
	}
	.navbar-dark .navbar-nav .nav-link {
    color: rgb(255, 255, 255);
	}
	.color-white {
		color: #fff;
	}
	.dropdown-control {
    margin-top: 20px;
    width: 215px !important;
	}
	.padding-control {
		padding: 0px 20px;
	}
	.bg-info {
    background-color: #024668 !important;
	}
	.consult {
		border: 2px solid white;
    border-radius: 10px;
    background-color: orangered;
    font-weight: 600;
	}
	.consult:hover {
		border: 2px solid white;
    border-radius: 10px;
    background-color: red;
    font-weight: 600;
	}
	.control-link {
    text-decoration: none;
    color: white;
	}
	@media screen and (max-width: 992px) {
		.consult {
			border: none;
			border-radius: none;
			background-color:transparent;
			font-weight: normal;
		}
		.consult:hover {
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
	}
</style>