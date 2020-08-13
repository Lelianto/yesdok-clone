<template>
  <div>
    <div>
      <Header />
      <div class="container">
        <div class="row">
          <div class="col-lg-2 col-1">
          </div>
          <div class="col-lg-8 col-10">
            <Detail :detailArticle="detailArticle"/>
          </div>
          <div class="col-lg-2 col-1">
          </div>
        </div>
      </div>
      <Footer/>
    </div>
  </div>
</template>

<script>
import Header from '@/components/header/index.vue';
import Detail from '@/components/detail/index.vue';
import Footer from '@/components/footer/index.vue';
export default {
  data() {
    return {
      detailArticle:{},
      articles: [
        {
          title: 'Mengapa Anda Terbangun Dengan Kepala Sakit',
          photo: 'https://www.yesdok.com/visual/slideshow/sakit%20kepala-article-1597058940.jpg',
          text: ['Seharian di rumah membuat Anda jadi terus-menerus tidur? Memang, ketika sudah disibukkan dengan berbagai aktivitas, tidur merupakan suatu barang mewah yang sulit didapatkan. Inilah yang membuat banyak orang “membalas dendam” untuk tidur lebih lama ketika terdapat hari libur atau akhir pekan.', 'Seharian di rumah membuat Anda jadi terus-menerus tidur? Memang, ketika sudah disibukkan dengan berbagai aktivitas, tidur merupakan suatu barang mewah yang sulit didapatkan. Inilah yang membuat banyak orang “membalas dendam” untuk tidur lebih lama ketika terdapat hari libur atau akhir pekan.', 'Seharian di rumah membuat Anda jadi terus-menerus tidur? Memang, ketika sudah disibukkan dengan berbagai aktivitas, tidur merupakan suatu barang mewah yang sulit didapatkan. Inilah yang membuat banyak orang “membalas dendam” untuk tidur lebih lama ketika terdapat hari libur atau akhir pekan.', 'Seharian di rumah membuat Anda jadi terus-menerus tidur? Memang, ketika sudah disibukkan dengan berbagai aktivitas, tidur merupakan suatu barang mewah yang sulit didapatkan. Inilah yang membuat banyak orang “membalas dendam” untuk tidur lebih lama ketika terdapat hari libur atau akhir pekan.'],
          type: 'Sehat A-Z',
          date: '12 AUG 2020'
        },
        {
          title: 'Terlalu Lama Menatap Smartphone Bisa Jadi Penyebab Mata Kering',
          photo: 'https://www.yesdok.com/visual/slideshow/1610-article-1597078202.jpg',
          text: ['Tidak ada penyebab yang sama untuk setiap orang yang memiliki mata kering. Penuaan adalah salah satu penyebab utamanya, bersamaan dengan penurunan produksi air mata Anda.', 'Tidak ada penyebab yang sama untuk setiap orang yang memiliki mata kering. Penuaan adalah salah satu penyebab utamanya, bersamaan dengan penurunan produksi air mata Anda.', 'Tidak ada penyebab yang sama untuk setiap orang yang memiliki mata kering. Penuaan adalah salah satu penyebab utamanya, bersamaan dengan penurunan produksi air mata Anda.', 'Tidak ada penyebab yang sama untuk setiap orang yang memiliki mata kering. Penuaan adalah salah satu penyebab utamanya, bersamaan dengan penurunan produksi air mata Anda.'],
          type: 'Gaya Hidup',
          date: '12 AUG 2020'
        },
        {
          title: 'Tips Perawatan Kulit Dengan Buah Apel',
          photo: 'https://www.yesdok.com/visual/slideshow/apel-article-1597059020.jpg',
          text: ['Siapa suka buah apel? Buah berwarna merah dan hijau ini disukai oleh banyak orang karena rasanya yang segar, manis, dan nikmat. Nutrisi dalam buah apel juga membuat buah ini sehat untuk dikonsumsi setiap hari.', 'Tidak ada penyebab yang sama untuk setiap orang yang memiliki mata kering. Penuaan adalah salah satu penyebab utamanya, bersamaan dengan penurunan produksi air mata Anda.', 'Tidak ada penyebab yang sama untuk setiap orang yang memiliki mata kering. Penuaan adalah salah satu penyebab utamanya, bersamaan dengan penurunan produksi air mata Anda.', 'Tidak ada penyebab yang sama untuk setiap orang yang memiliki mata kering. Penuaan adalah salah satu penyebab utamanya, bersamaan dengan penurunan produksi air mata Anda.'],
          type: 'Gaya Hidup',
          date: '10 AUG 2020'
        },
        {
          title: 'Meluruskan Kesalahpahaman Terkait Thermo Gun',
          photo: 'https://www.yesdok.com/visual/slideshow/1578581508-article-1597034350.jpg',
          text: ['Salah satu gejala infeksi virus Covid 19 adalah demam atau peningkatan suhu tubuh. Ini melatarbelakangi pengecekan suhu tubuh dengan menggunakan thermo gun saat individu akan memasuki kawasan kantor atau fasilitas umum.', 'Salah satu gejala infeksi virus Covid 19 adalah demam atau peningkatan suhu tubuh. Ini melatarbelakangi pengecekan suhu tubuh dengan menggunakan thermo gun saat individu akan memasuki kawasan kantor atau fasilitas umum.', 'Salah satu gejala infeksi virus Covid 19 adalah demam atau peningkatan suhu tubuh. Ini melatarbelakangi pengecekan suhu tubuh dengan menggunakan thermo gun saat individu akan memasuki kawasan kantor atau fasilitas umum.', 'Salah satu gejala infeksi virus Covid 19 adalah demam atau peningkatan suhu tubuh. Ini melatarbelakangi pengecekan suhu tubuh dengan menggunakan thermo gun saat individu akan memasuki kawasan kantor atau fasilitas umum.'],
          type: 'Terkini',
          date: '11 AUG 2020'
        },
        {
          title: 'Apakah Minum Air Panas Bantu Hilangkan Lemak Di Perut?',
          photo: 'https://www.yesdok.com/visual/slideshow/0a5c95d9-2f58-4ecd-b17a-17e11c2cdb46-article-1596978080.jpeg',
          text: ['Bukan rahasia lagi bahwa air sangat penting untuk kelangsungan hidup manusia. Sekitar 70 persen tubuh manusia terdiri dari air dan untuk menjaga sistem tubuh bekerja secara efisien, setiap orang dewasa perlu mengonsumsi setidaknya 2-3 liter air setiap hari. Air bukan hanya karena memuaskan dahaga, tetapi juga diperlukan untuk berfungsinya bagi tubuh dalam mencegah penyakit.', 'Bukan rahasia lagi bahwa air sangat penting untuk kelangsungan hidup manusia. Sekitar 70 persen tubuh manusia terdiri dari air dan untuk menjaga sistem tubuh bekerja secara efisien, setiap orang dewasa perlu mengonsumsi setidaknya 2-3 liter air setiap hari. Air bukan hanya karena memuaskan dahaga, tetapi juga diperlukan untuk berfungsinya bagi tubuh dalam mencegah penyakit.', 'Bukan rahasia lagi bahwa air sangat penting untuk kelangsungan hidup manusia. Sekitar 70 persen tubuh manusia terdiri dari air dan untuk menjaga sistem tubuh bekerja secara efisien, setiap orang dewasa perlu mengonsumsi setidaknya 2-3 liter air setiap hari. Air bukan hanya karena memuaskan dahaga, tetapi juga diperlukan untuk berfungsinya bagi tubuh dalam mencegah penyakit.', 'Bukan rahasia lagi bahwa air sangat penting untuk kelangsungan hidup manusia. Sekitar 70 persen tubuh manusia terdiri dari air dan untuk menjaga sistem tubuh bekerja secara efisien, setiap orang dewasa perlu mengonsumsi setidaknya 2-3 liter air setiap hari. Air bukan hanya karena memuaskan dahaga, tetapi juga diperlukan untuk berfungsinya bagi tubuh dalam mencegah penyakit.', 'Bukan rahasia lagi bahwa air sangat penting untuk kelangsungan hidup manusia. Sekitar 70 persen tubuh manusia terdiri dari air dan untuk menjaga sistem tubuh bekerja secara efisien, setiap orang dewasa perlu mengonsumsi setidaknya 2-3 liter air setiap hari. Air bukan hanya karena memuaskan dahaga, tetapi juga diperlukan untuk berfungsinya bagi tubuh dalam mencegah penyakit.', 'Bukan rahasia lagi bahwa air sangat penting untuk kelangsungan hidup manusia. Sekitar 70 persen tubuh manusia terdiri dari air dan untuk menjaga sistem tubuh bekerja secara efisien, setiap orang dewasa perlu mengonsumsi setidaknya 2-3 liter air setiap hari. Air bukan hanya karena memuaskan dahaga, tetapi juga diperlukan untuk berfungsinya bagi tubuh dalam mencegah penyakit.', 'Bukan rahasia lagi bahwa air sangat penting untuk kelangsungan hidup manusia. Sekitar 70 persen tubuh manusia terdiri dari air dan untuk menjaga sistem tubuh bekerja secara efisien, setiap orang dewasa perlu mengonsumsi setidaknya 2-3 liter air setiap hari. Air bukan hanya karena memuaskan dahaga, tetapi juga diperlukan untuk berfungsinya bagi tubuh dalam mencegah penyakit.'],
          type: 'Diet',
          date: '11 AUG 2020'
        },
        {
          title: 'Mengapa Anda Terbangun Dengan Kepala Sakit',
          photo: 'https://www.yesdok.com/visual/slideshow/kiwi-3614078_640-article-1591782250.jpg',
          text: ['Seharian di rumah membuat Anda jadi terus-menerus tidur? Memang, ketika sudah disibukkan dengan berbagai aktivitas, tidur merupakan suatu barang mewah yang sulit didapatkan. Inilah yang membuat banyak orang “membalas dendam” untuk tidur lebih lama ketika terdapat hari libur atau akhir pekan.', 'Bukan rahasia lagi bahwa air sangat penting untuk kelangsungan hidup manusia. Sekitar 70 persen tubuh manusia terdiri dari air dan untuk menjaga sistem tubuh bekerja secara efisien, setiap orang dewasa perlu mengonsumsi setidaknya 2-3 liter air setiap hari. Air bukan hanya karena memuaskan dahaga, tetapi juga diperlukan untuk berfungsinya bagi tubuh dalam mencegah penyakit.', 'Bukan rahasia lagi bahwa air sangat penting untuk kelangsungan hidup manusia. Sekitar 70 persen tubuh manusia terdiri dari air dan untuk menjaga sistem tubuh bekerja secara efisien, setiap orang dewasa perlu mengonsumsi setidaknya 2-3 liter air setiap hari. Air bukan hanya karena memuaskan dahaga, tetapi juga diperlukan untuk berfungsinya bagi tubuh dalam mencegah penyakit.', 'Bukan rahasia lagi bahwa air sangat penting untuk kelangsungan hidup manusia. Sekitar 70 persen tubuh manusia terdiri dari air dan untuk menjaga sistem tubuh bekerja secara efisien, setiap orang dewasa perlu mengonsumsi setidaknya 2-3 liter air setiap hari. Air bukan hanya karena memuaskan dahaga, tetapi juga diperlukan untuk berfungsinya bagi tubuh dalam mencegah penyakit.'],
          type: 'Sehat A-Z',
          date: '12 AUG 2020'
        },
        {
          title: 'Terlalu Lama Menatap Smartphone Bisa Jadi Penyebab Mata Kering',
          photo: 'https://www.yesdok.com/visual/slideshow/fdfd-article-1594815351.jpg',
          text: ['Tidak ada penyebab yang sama untuk setiap orang yang memiliki mata kering. Penuaan adalah salah satu penyebab utamanya, bersamaan dengan penurunan produksi air mata Anda.', 'Tidak ada penyebab yang sama untuk setiap orang yang memiliki mata kering. Penuaan adalah salah satu penyebab utamanya, bersamaan dengan penurunan produksi air mata Anda.', 'Tidak ada penyebab yang sama untuk setiap orang yang memiliki mata kering. Penuaan adalah salah satu penyebab utamanya, bersamaan dengan penurunan produksi air mata Anda.', 'Tidak ada penyebab yang sama untuk setiap orang yang memiliki mata kering. Penuaan adalah salah satu penyebab utamanya, bersamaan dengan penurunan produksi air mata Anda.'],
          type: 'Gaya Hidup',
          date: '12 AUG 2020'
        },
        {
          title: 'Tips Perawatan Kulit Dengan Buah Apel',
          photo: 'https://www.yesdok.com/visual/slideshow/article_095d324b10afe3890b2c8a50b52635b49df23093.jpg',
          text: ['Siapa suka buah apel? Buah berwarna merah dan hijau ini disukai oleh banyak orang karena rasanya yang segar, manis, dan nikmat. Nutrisi dalam buah apel juga membuat buah ini sehat untuk dikonsumsi setiap hari.', 'Siapa suka buah apel? Buah berwarna merah dan hijau ini disukai oleh banyak orang karena rasanya yang segar, manis, dan nikmat. Nutrisi dalam buah apel juga membuat buah ini sehat untuk dikonsumsi setiap hari.', 'Siapa suka buah apel? Buah berwarna merah dan hijau ini disukai oleh banyak orang karena rasanya yang segar, manis, dan nikmat. Nutrisi dalam buah apel juga membuat buah ini sehat untuk dikonsumsi setiap hari.', 'Siapa suka buah apel? Buah berwarna merah dan hijau ini disukai oleh banyak orang karena rasanya yang segar, manis, dan nikmat. Nutrisi dalam buah apel juga membuat buah ini sehat untuk dikonsumsi setiap hari.'],
          type: 'Gaya Hidup',
          date: '10 AUG 2020'
        },
      ]
    };
  },
  mounted() {
    if (this.$route.query.id) {
      this.detailArticle = this.articles[this.$route.query.id]
    } else {
      this.$router.push('/')
    }
  }
}
</script>

<style>
  .container {
    margin: 0 auto;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
  }

  .title {
    font-family:
      'Quicksand',
      'Source Sans Pro',
      -apple-system,
      BlinkMacSystemFont,
      'Segoe UI',
      Roboto,
      'Helvetica Neue',
      Arial,
      sans-serif;
    display: block;
    font-weight: 300;
    font-size: 100px;
    color: #35495e;
    letter-spacing: 1px;
  }

  .subtitle {
    font-weight: 300;
    font-size: 42px;
    color: #526488;
    word-spacing: 5px;
    padding-bottom: 15px;
  }

  .links {
    padding-top: 15px;
  }

  .card-section {
    padding-top: 90px;
  }
</style>
