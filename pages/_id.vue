<template>
  <div>
    <div>
      <Header />
      <Footer/>
    </div>
  </div>
</template>

<script>
import Header from '@/components/header/index.vue';
import Footer from '@/components/footer/index.vue'
export default {
  data() {
    return {
    }
	},
	mounted() {
		/**
		 * This page just for handling random path error
		 * We usually use middleware if there is any token that we use
		 */
		this.$router.push('/')
	}
}
</script>
