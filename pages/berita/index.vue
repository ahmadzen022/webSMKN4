<template>
  <div class="container ">
    <h1 class="text-center">Berita Terbaru</h1>
    <div class="row pt-5">
      <!-- Berita pertama di kiri -->
      <div class="col-md-6 mb-3">
        <div v-for="(berita, index) in beritaListkiri" :key="index" class="card mb-3 shadow-sm berita-card">
          <div class="row no-gutters">
            <div class="col-md-4">
              <img :src="berita.foto" class="card-img" alt="Gambar Berita" />
            </div>
            <div class="col-md-8">
              <div class="card-body">
                <h5 class="card-title">{{ berita.judul }}</h5>
                <h6 class="card-subtitle mb-2 text-muted">{{ berita.tanggal }}</h6>
                <p class="card-text">{{ berita.deskripsi }}</p>
                <a :href="berita.link" target="_blank" class="card-link">Baca Selengkapnya</a>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Berita kedua di kanan -->
      <div class="col-md-6 mb-3">
        <div v-for="(berita, index) in beritaListKanan" :key="'right-' + index" class="card mb-3 shadow-sm berita-card">
          <div class="row no-gutters">
                  <div class="col-md-4">
                      <img :src="berita.foto" class="card-img" alt="Gambar Berita" />
                  </div>
                  <div class="col-md-8">
                      <div class="card-body">
                          <h5 class="card-title">{{ berita.judul }}</h5>
                          <h6 class="card-subtitle mb-2 text-muted">{{ berita.tanggal }}</h6>
                          <p class="card-text">{{ berita.deskripsi }}</p>
                          <a :href="berita.link" target="_blank" class="card-link">Baca Selengkapnya</a>
                      </div>
                  </div>  
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import foto1 from '@/assets/berita/astra.jpg'
import foto2 from '@/assets/berita/gur.jpeg'
import foto3 from '@/assets/berita/jo.jpg'
const beritaListkiri = [
{
    judul: 'SMKN 4 Tasikmalaya Gelar Job Fair 2023, Harapkan Angka Pengangguran di Tasikmalaya Berkurang',
    tanggal: '12/10/2024',
    deskripsi: 'Job Fair 2023 yang membutuhkan sebanyak 540....',
    foto: foto3, // Gambar berita
    link: 'https://ruangatas.com/smkn-4-tasikmalaya-gelar-job-fair-2023-harapkan-angka-pengangguran-di-tasikmalaya-berkurang/' // Link ke halaman eksternal
  },
  {
    judul: 'Sinkronisasi Kurikulum SMKN 4 Tasikmalaya dengan Inovindo',
    tanggal: '09/07/2024',
    deskripsi: 'Sekolah Menengah Kejuruan Negeri 4 Tasikmalaya (SMKN 4 Tasikmalaya)...',
    foto: foto2, // Gambar berita
    link: 'https://inovindoacademy.com/berita/sinkronisasi-kurikulum-smkn-4-tasikmalaya-dengan-inovindo' // Link ke halaman eksternal
  },
  {
    judul: 'Astra Honda Resmikan Safety Riding Lab ke-7 di SMKN 4 Tasikmalaya, Kampanye Keselamatan Berkendara',
    tanggal: '20/05/2024',
    deskripsi: 'Yayasan Astra Honda Motor (AHM) meresmikan Safety Riding Lab...',
    foto: foto1, // Gambar berita
    link: 'https://inovindoacademy.com/berita/sinkronisasi-kurikulum-smkn-4-tasikmalaya-dengan-inovindo' // Link ke halaman eksternal
  }
];
const beritaListKanan = [
{
    judul: 'SMKN 4 Tasikmalaya Gelar Job Fair 2023, Harapkan Angka Pengangguran di Tasikmalaya Berkurang',
    tanggal: '12/10/2024',
    deskripsi: 'Job Fair 2023 yang membutuhkan sebanyak 540....',
    foto: foto3, // Gambar berita
    link: 'https://ruangatas.com/smkn-4-tasikmalaya-gelar-job-fair-2023-harapkan-angka-pengangguran-di-tasikmalaya-berkurang/' // Link ke halaman eksternal
  },
  {
    judul: 'Sinkronisasi Kurikulum SMKN 4 Tasikmalaya dengan Inovindo',
    tanggal: '09/07/2024',
    deskripsi: 'Sekolah Menengah Kejuruan Negeri 4 Tasikmalaya (SMKN 4 Tasikmalaya)...',
    foto: foto2, // Gambar berita
    link: 'https://inovindoacademy.com/berita/sinkronisasi-kurikulum-smkn-4-tasikmalaya-dengan-inovindo' // Link ke halaman eksternal
  },
  {
    judul: 'Astra Honda Resmikan Safety Riding Lab ke-7 di SMKN 4 Tasikmalaya, Kampanye Keselamatan Berkendara',
    tanggal: '20/05/2024',
    deskripsi: 'Yayasan Astra Honda Motor (AHM) meresmikan Safety Riding Lab...',
    foto: foto1, // Gambar berita
    link: 'https://inovindoacademy.com/berita/sinkronisasi-kurikulum-smkn-4-tasikmalaya-dengan-inovindo' // Link ke halaman eksternal
  }

]
</script>

<style scoped>
.container {
  padding-top: 140px;
}
/* Mengurangi ukuran card */
.berita-card {
width: 100%; /* Lebar card tetap penuh */
max-width: 600px; /* Membatasi lebar maksimal */
margin: 0 auto; /* Agar card terpusat */
}

.card {
transition: transform 0.2s ease-in-out;
}

.card:hover {
transform: scale(1.05);
}

/* Mengatur ukuran gambar agar proporsional */
.card-img {
width: 100%; /* Mengatur lebar gambar agar sesuai dengan kolom */
height: 200px; /* Menentukan tinggi gambar yang lebih tinggi untuk menyesuaikan */
object-fit: cover; /* Menjaga proporsi gambar dan memotong jika perlu */
}

/* Pastikan gambar tetap pas dalam kolom */
.card-body {
padding: 15px; /* Mengurangi padding pada card */
}

.card-title {
font-size: 1.1rem; /* Ukuran judul lebih kecil */
}

.card-link:hover {
text-decoration: underline;
}

</style>
