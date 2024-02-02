<template>
<div class="container">
        <div class="section-title">
          <h2>Portfolio</h2>
          <!-- <p>My Works</p> -->
        </div>
        <div class="row">
          <div class="col-lg-12 d-flex justify-content-center">
            <ul id="portfolio-flters">
              <li data-filter="*" class="filter-active">All</li>
              <!-- <li data-filter=".filter-app">App</li>
              <li data-filter=".filter-card">Card</li>
              <li data-filter=".filter-web">Web</li> -->
            </ul>
          </div>
        </div>

        <div class="row portfolio-container">

            <div class="col-lg-6 col-md-6 portfolio-item filter-app" v-for="(item, index) in porfolioData" :key="index">
            <div class="portfolio-wrap">
                <img :src="item.img[0]" class="img-fluid" alt="">
                <div class="portfolio-info">
                <h4>{{item.title}}</h4>
                <p>{{item.type}}</p>
                <div class="portfolio-links">
                    <a href="#" @click="$bvModal.show(`bv-modal-${index}`)"><i class="bx bx-link"></i></a>
                    <b-modal :id="`bv-modal-${index}`" size="xl" :title="`Detail ( ${item.title} )`">
                        <div class="row mx-4">
                            <h4 class="text-center text-dark font-weight-bold">{{item.title}}</h4>
                            <p class="my-4 text-secondary">Tools : {{item.tools}}</p>
                            <div class="col-xl-6 col-lg-6 col-md-6 col-sm-12" v-for="(img, indexImg) in item.img"  :key="indexImg">
                                <img class="w-100 my-2" :src="img" alt="" srcset="">
                            </div>
                            <hr>
                            <p class="text-dark"> {{item.desc.parent}} </p> 
                            <ul class="text-dark px-4">
                                <li v-for="(sub, indexDesc) in item.desc.sub" :key="indexDesc">{{sub}}</li>
                            </ul>
                        </div>
                    <template #modal-footer="{ ok}">
                        <b-button size="sm" variant="success" @click="ok()">
                            OK
                        </b-button>
                    </template>
                    </b-modal>
                </div>
                </div>
            </div>
            </div>

        </div>

      </div>
</template>

<script>
export default {
    name: 'SERVICE',
    data() {
        return {
            porfolioData: [
                {
                    title : 'LSP Geti - ATT GROUP',
                    type : 'Web App',
                    tools: 'Laravel, Nuxt.js, SQL',
                    img : [
                        '/template/assets/img/portfolio/lsp/lsp.jpg',
                        '/template/assets/img/portfolio/lsp/1.jpg'
                    ],
                    desc: {
                        parent: 'Program yang dibuat untuk kebuTuhan LSP yang dilakukan secara Online. dimana asesi diberikan ditunjukan soal-soal Tertulis, atau praktek(diberi link zoom) dan diawasi oleh asesor yang data master tersebut dibuat dan bisa dikelola oleh user admin ',
                        sub: [
                            'Tediri dari 3 user Asesi, Asesor, Admin',
                            'Menggunakan fitur socket untuk kebutuhan data secara live',
                            'Terdapat Fitur Notifikasi',
                            'Terdapat fitur untuk tanda tangan secara online'
                        ]
                    }
                    
                },

               

                {
                    title : 'Receiving App - Sarirasa Group',
                    tools: 'Express.js, Vue.js, SQL, Mongo, Bootstrap',
                    type : 'Web App',
                    img : [
                        '/template/assets/img/portfolio/receiving/receiving.PNG',
                        '/template/assets/img/portfolio/receiving/receiving1.PNG',
                    ],
                    desc: {
                        parent: 'Program ini dibuat untuk Transaksi pada penerimaan barang di Gudang Sarirasa Group, pada transaksi ini barang yang diterima akan dikategorikan kedalam beberapa grade setelah itu barang ditimbang, dan di qc, dan terdapat proses akhir untuk perubahan data menjadi pack, yang nantinya akan masuk pada data penerimaan barang.',
                    }
                    
                },
                {
                    title : 'Dsitribusi App - Sarirasa Group',
                    tools: 'Express.js, Vue.js, SQL, Mongo, Bootstrap',
                    type : 'Web App',
                    img : [
                        '/template/assets/img/portfolio/distribusi/distribusi.PNG',
                        // '/template/assets/img/portfolio/distribusi/distribusi1.PNG',
                    ],
                    desc: {
                        parent: 'Program ini dibuat untuk Transaksi pada Distribusi produk dari Gudang Sarirasa Group ke Store Sarirasa, produk yang sudah diterima digudang akan di sebar atau didistribusikan sesuai dengan order dari masing-masing store. pada transaksi ini melalui proses picking, lalu dibuat no SKB, setelah itu melalui proses Distribusi terima, proses split barang ke kontainer, dan terakhir pembuatan surat SKB transit sebagai pembuktian untuk pengiriman barang menuju lokasi store. ',
                    }
                    
                },
                {
                    title : 'Web boh - Sarirasa Group',
                    tools: 'Express.js, Vue.js, SQL, Mongo, Bootstrap',
                    type : 'Web App',
                    img : [
                        '/template/assets/img/portfolio/weboh/weboh.PNG',
                        '/template/assets/img/portfolio/weboh/weboh2.PNG',
                    ],
                    desc: {
                        parent: 'Program ini dibuat untuk mengelola data Produk dan sub produk yang ada di menu POS pada brand yang tersedia di Sarirasa group terkait produk apa saja yang tampil, Promosi, Harga, dsb',
                    }
                    
                },

               
               
                {
                    title : 'Nomads App - Course',
                    tools: 'Laravel, Bootstrap, SQL, Midtrans',
                    type : 'Web App',
                    img : [
                        '/template/assets/img/portfolio/nomads/nomads.jpg',
                        '/template/assets/img/portfolio/nomads/1.jpg'
                    ],
                    desc: {
                        parent: 'Program ini merupakan program yang dibuat untuk e-commerce pada travel. jadi terdapat 2 pengguna yaitu admin dan user. pengguna admin untuk mengatur dan mengolola data untuk travel, sedangkan user yang membeli travel yang ada. ',
                        sub: [
                            'Authentication, terdapat 2 pengguna',
                            'Menu untuk kelola data travel',
                            'Menu untuk upload gambar',
                            'Terintegrasi dengan Midtrans'
                        ]
                    }
                    
                },
                {
                    title : 'Shayna App - Course',
                    tools: 'Laravel, Vue.js, SQL, Bootstrap',
                    type : 'Web App',
                    img : [
                        '/template/assets/img/portfolio/shayna/shayna.jpg',
                        '/template/assets/img/portfolio/shayna/1.jpg'
                    ],
                    desc: {
                        parent: 'Program yang dibuat untuk E-commerce atau jual beli barang secara online berbasis website dengan memanfaatkan Framework Laravel sebagai Back-End dan Vue Js sebagai Front-End. Terdapat 2 pengguna pada website ini yaitu Admin dan User. Website ini memiliki beberapa fitur sebagai berikut: Website ini memiliki beberapa fitur diantaranya,',
                        sub: [
                            'Fitur multi-user di Situs Web',
                            'Panel Admin (CMS) untuk mengelola data',
                            'Menu untuk mengelola data Produk',
                            'Bisa Upload Gambar untuk foto produk',
                        ]
                    }
                    
                },

                {
                    title : 'Lost Items App - Freelance',
                    tools: 'Laravel, SQL, Bootstrap',
                    type : 'Web App',
                    img : [
                        '/template/assets/img/portfolio/lost_items/lost_item.jpg',
                        '/template/assets/img/portfolio/lost_items/1.jpg'
                    ],
                    desc: {
                        parent: 'This program is a website-based program created to search for and find lost items, along with some of the features in this program',
                        sub: [
                            'Authentication',
                            'Feature Crud Item with multiple image',
                            'Feature Manipulation data in user'
                        ]
                    }
                    
                },
              
              
               
              
               
            ]
        }
    },
}
</script>

<style>

</style>