<template>
  <div>
    <div>
      <Header />
      <div class="container-fluid slide-section">
        <div class="row">
          <div class="col-lg-8 col-12 padding-zero">
            <Slider :src="src1" :caption="caption"/>
          </div>
          <div class="col-lg-4 col-12">
            <div class="row padding-zero">
              <div class="col-lg-12 col-6 padding-zero">
                <Slider :src="src2" :caption="caption"/>
              </div>
              <div class="col-lg-12 col-6 padding-zero">
                <Slider :src="src3" :caption="caption"/>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="control-text">
        Butuh Artikel Terpercaya? <br> Baca Artikel di Bawah ini!
      </div>
      <div class="container-fluid card-section">
        <div class='row'>
          <div v-for="(article, index) in articles" :key="index" class="col-lg-3 col-md-6 col-sm-12 col-12">
            <Card :article="article" :index="index"/>
          </div>
        </div>
      </div>
      <Footer/>
    </div>
  </div>
</template>

<script>
import Header from '@/components/header/index.vue';
import Slider from '@/components/slider/index.vue';
import Card from '@/components/card/index.vue';
import Footer from '@/components/footer/index.vue'
export default {
  data() {
    return {
      articles: [
        {
          title: 'Mengapa Anda Terbangun Dengan Kepala Sakit',
          photo: 'https://www.yesdok.com/visual/slideshow/sakit%20kepala-article-1597058940.jpg',
          text: 'Seharian di rumah membuat Anda jadi terus-menerus tidur? Memang, ketika sudah disibukkan dengan berbagai aktivitas, tidur merupakan suatu barang mewah yang sulit didapatkan. Inilah yang membuat banyak orang “membalas dendam” untuk tidur lebih lama ketika terdapat hari libur atau akhir pekan.',
          type: 'Sehat A-Z',
          date: '12 AUG 2020'
        },
        {
          title: 'Terlalu Lama Menatap Smartphone Bisa Jadi Penyebab Mata Kering',
          photo: 'https://www.yesdok.com/visual/slideshow/1610-article-1597078202.jpg',
          text: 'Tidak ada penyebab yang sama untuk setiap orang yang memiliki mata kering. Penuaan adalah salah satu penyebab utamanya, bersamaan dengan penurunan produksi air mata Anda.',
          type: 'Gaya Hidup',
          date: '12 AUG 2020'
        },
        {
          title: 'Tips Perawatan Kulit Dengan Buah Apel',
          photo: 'https://www.yesdok.com/visual/slideshow/apel-article-1597059020.jpg',
          text: 'Siapa suka buah apel? Buah berwarna merah dan hijau ini disukai oleh banyak orang karena rasanya yang segar, manis, dan nikmat. Nutrisi dalam buah apel juga membuat buah ini sehat untuk dikonsumsi setiap hari.',
          type: 'Gaya Hidup',
          date: '10 AUG 2020'
        },
        {
          title: 'Meluruskan Kesalahpahaman Terkait Thermo Gun',
          photo: 'https://www.yesdok.com/visual/slideshow/1578581508-article-1597034350.jpg',
          text: 'Salah satu gejala infeksi virus Covid 19 adalah demam atau peningkatan suhu tubuh. Ini melatarbelakangi pengecekan suhu tubuh dengan menggunakan thermo gun saat individu akan memasuki kawasan kantor atau fasilitas umum.',
          type: 'Terkini',
          date: '11 AUG 2020'
        },
        {
          title: 'Apakah Minum Air Panas Bantu Hilangkan Lemak Di Perut?',
          photo: 'https://www.yesdok.com/visual/slideshow/0a5c95d9-2f58-4ecd-b17a-17e11c2cdb46-article-1596978080.jpeg',
          text: 'Bukan rahasia lagi bahwa air sangat penting untuk kelangsungan hidup manusia. Sekitar 70 persen tubuh manusia terdiri dari air dan untuk menjaga sistem tubuh bekerja secara efisien, setiap orang dewasa perlu mengonsumsi setidaknya 2-3 liter air setiap hari. Air bukan hanya karena memuaskan dahaga, tetapi juga diperlukan untuk berfungsinya bagi tubuh dalam mencegah penyakit.',
          type: 'Diet',
          date: '11 AUG 2020'
        },
        {
          title: 'Mengapa Anda Terbangun Dengan Kepala Sakit',
          photo: 'https://www.yesdok.com/visual/slideshow/kiwi-3614078_640-article-1591782250.jpg',
          text: 'Seharian di rumah membuat Anda jadi terus-menerus tidur? Memang, ketika sudah disibukkan dengan berbagai aktivitas, tidur merupakan suatu barang mewah yang sulit didapatkan. Inilah yang membuat banyak orang “membalas dendam” untuk tidur lebih lama ketika terdapat hari libur atau akhir pekan.',
          type: 'Sehat A-Z',
          date: '12 AUG 2020'
        },
        {
          title: 'Terlalu Lama Menatap Smartphone Bisa Jadi Penyebab Mata Kering',
          photo: 'https://www.yesdok.com/visual/slideshow/fdfd-article-1594815351.jpg',
          text: 'Tidak ada penyebab yang sama untuk setiap orang yang memiliki mata kering. Penuaan adalah salah satu penyebab utamanya, bersamaan dengan penurunan produksi air mata Anda.',
          type: 'Gaya Hidup',
          date: '12 AUG 2020'
        },
        {
          title: 'Tips Perawatan Kulit Dengan Buah Apel',
          photo: 'https://www.yesdok.com/visual/slideshow/article_095d324b10afe3890b2c8a50b52635b49df23093.jpg',
          text: 'Siapa suka buah apel? Buah berwarna merah dan hijau ini disukai oleh banyak orang karena rasanya yang segar, manis, dan nikmat. Nutrisi dalam buah apel juga membuat buah ini sehat untuk dikonsumsi setiap hari.',
          type: 'Gaya Hidup',
          date: '10 AUG 2020'
        },
      ],
      src1: [
        'https://firebasestorage.googleapis.com/v0/b/xendit-f789a.appspot.com/o/1.jpg?alt=media&token=ff19b723-2f54-4263-b816-02600ebc4035',
        'https://firebasestorage.googleapis.com/v0/b/xendit-f789a.appspot.com/o/3.jpg?alt=media&token=0e91985e-bd86-423a-bac4-c65b3bfb56f7',
        'https://firebasestorage.googleapis.com/v0/b/xendit-f789a.appspot.com/o/5.jpg?alt=media&token=11dcd229-9226-432c-95e1-ff4ed43b8887',
        'https://firebasestorage.googleapis.com/v0/b/xendit-f789a.appspot.com/o/7.jpg?alt=media&token=fb711758-d765-4812-9b50-bf26058616a2',
      ],
      src2: [
        'https://firebasestorage.googleapis.com/v0/b/xendit-f789a.appspot.com/o/2.jpg?alt=media&token=ac4548ea-f445-48bf-8afa-e67bdd7f1cfb',
        'https://firebasestorage.googleapis.com/v0/b/xendit-f789a.appspot.com/o/4.jpg?alt=media&token=23928d6d-20dd-4d6b-a16c-354dba755805',
        'https://firebasestorage.googleapis.com/v0/b/xendit-f789a.appspot.com/o/6.jpg?alt=media&token=13759ac1-55e5-4709-8b64-1339a07c9d7f',
        'https://firebasestorage.googleapis.com/v0/b/xendit-f789a.appspot.com/o/8.jpg?alt=media&token=7204991b-4969-43fc-9c83-8c1d5b1a1869',
      ],
      src3: [
        'https://firebasestorage.googleapis.com/v0/b/xendit-f789a.appspot.com/o/3.jpg?alt=media&token=0e91985e-bd86-423a-bac4-c65b3bfb56f7',
        'https://firebasestorage.googleapis.com/v0/b/xendit-f789a.appspot.com/o/7.jpg?alt=media&token=fb711758-d765-4812-9b50-bf26058616a2',
        'https://firebasestorage.googleapis.com/v0/b/xendit-f789a.appspot.com/o/4.jpg?alt=media&token=23928d6d-20dd-4d6b-a16c-354dba755805',
        'https://firebasestorage.googleapis.com/v0/b/xendit-f789a.appspot.com/o/1.jpg?alt=media&token=ff19b723-2f54-4263-b816-02600ebc4035',
      ],
      caption: [
        'Kesehatan',
        'Konsultasi',
        'Gaya Hidup',
        'Berita Terkini'
      ]
    };
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
    padding-top: 40px !important;
  }
  .slide-section{
    padding-top: 75px;
  }
  .padding-zero {
    padding: 0;
  }
  .control-text {
    margin-top: 50px;
    display: flex;
    justify-content: center;
    font-size: 32px;
    font-weight: bold;
  }
  @media screen and (max-width: 992px) {
		.control-text {
      margin-top: 10px;
      display: flex;
      justify-content: center;
      font-size: 24px;
      font-weight: bold;
    }
    .card-section {
      padding-top: 30px !important;
    }
	}
</style>
