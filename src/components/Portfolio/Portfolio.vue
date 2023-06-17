<template>
<div class="container">

        <div class="section-title">
          <h2>Portfolio</h2>
          <p>My Works</p>
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

          <div class="col-lg-4 col-md-6 portfolio-item filter-app" v-for="(item, index) in porfolioData" :key="index">
            <div class="portfolio-wrap">
              <img :src="item.img[0]" class="img-fluid" alt="">
              <div class="portfolio-info">
                <h4>{{item.title}}</h4>
                <p>{{item.type}}</p>
                <div class="portfolio-links">
                    <a href="#" @click="$bvModal.show(`bv-modal-${index}`)"><i class="bx bx-link"></i></a>
                    <b-modal :id="`bv-modal-${index}`" size="xl" :title="`Detail ( ${item.title} )`">
                    <p class="my-4 text-secondary">Tools : {{item.tools}}</p>
                    <div>
                        <img v-for="(img, indexImg) in item.img" :key="indexImg" class="img-thumbnail" style="width:50%" :src="img" alt="" srcset="">
                    </div>
                    <hr>
                        {{item.desc.parent}}
                        <ul>
                            <li v-for="(sub, indexDesc) in item.desc.sub" :key="indexDesc">{{sub}}</li>
                        </ul>
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
                    title : 'LSP Geti',
                    type : 'Web App',
                    tools: 'Laravel, Nuxt.js, SQL',
                    img : [
                        '/template/assets/img/portfolio/lsp/lsp.jpg',
                        '/template/assets/img/portfolio/lsp/1.jpg'
                    ],
                    desc: {
                        parent: 'This program is a website-based program created to manage data related to the needs of Professional Certification Institutions (LSP). It has 3 users, namely Assessors as LSP participants, Assessors as LSP examiners, and Admins who manage LSP master data. This website uses Laravel framework technology, Nuxt JS, Bootstrap, and MySQL database. :',
                        sub: []
                    }
                    
                },
                {
                    title : 'Covid Tracking App',
                    tools: 'React.js, Bootstrap, Covid Api',
                    type : 'Web App',
                    img : [
                        '/template/assets/img/portfolio/covid/covid.jpg',
                        '/template/assets/img/portfolio/covid/1.jpg'
                    ],
                    desc: {
                        parent: 'This program is a website-based program created for tracking covid data to view data related to covid cases (Confirmed, Recovered, Deaths) in various countries. :',
                        sub: []
                    }
                    
                },
                {
                    title : 'Nomads App',
                    tools: 'Laravel, Bootstrap, SQL, Midtrans',
                    type : 'Web App',
                    img : [
                        '/template/assets/img/portfolio/nomads/nomads.jpg',
                        '/template/assets/img/portfolio/nomads/1.jpg'
                    ],
                    desc: {
                        parent: 'This website is a website created to manage travel ticket booking data by utilizing website technology using the Laravel Framework. This website has several features including,',
                        sub: [
                            'Multi user features on the Website',
                            'Menu for managing Travel data',
                            'Image upload feature',
                            'Already integrated with Midtrans'
                        ]
                    }
                    
                },
                {
                    title : 'Shayna App',
                    tools: 'Laravel, Vue.js, SQL, Bootstrap',
                    type : 'Web App',
                    img : [
                        '/template/assets/img/portfolio/shayna/shayna.jpg',
                        '/template/assets/img/portfolio/shayna/1.jpg'
                    ],
                    desc: {
                        parent: 'This program is a program for E-commerce or website-based online buying and selling of goods by utilizing the Laravel Framework as the Back-End and Vue Js as the Front-End. There are 2 users on this website, namely Admin and User. This website has the following features: This website has several features including,',
                        sub: [
                            'Multi user features on the Website',
                            'Admin Panel (CMS) to manage data',
                            'Menu for managing Product data',
                            'Can Upload Images for product photos',
                            'using API for manipulation data'
                        ]
                    }
                    
                },
                {
                    title : 'Laundry App',
                    tools: 'Laravel, SQL, Bootstrap',
                    type : 'Web App',
                    img : [
                        '/template/assets/img/portfolio/laundry/laundry.jpg',
                        '/template/assets/img/portfolio/laundry/1.jpg'
                    ],
                    desc: {
                        parent: 'apLaundry is a program created for an information system in a Laundry. The following features exist on this appLaundry website which has several features including:',
                        sub: [
                            'CRUD Customers',
                            'CRUD Transaction Laundry',
                            'Authentication',
                            'Feature Print',
                        ]
                    }
                    
                },
                {
                    title : 'Lost Items App',
                    tools: 'Laravel, SQL, Bootstrap',
                    type : 'Web App',
                    img : [
                        '/template/assets/img/portfolio/lost_item/lost_item.jpg',
                        '/template/assets/img/portfolio/lost_item/1.jpg'
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