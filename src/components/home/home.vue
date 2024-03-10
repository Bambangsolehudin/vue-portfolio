
<template>
<div class="container">
  <div class="row">
    <div class="navbar row ">
        <b-navbar class="" type="light" variant="light" fixed="bottom">
          <div class="col-12 d-flex justify-content-between ">
            <div class="w-25 text-center text-danger">
              <i class="fa-solid fa-house"></i> <br>
              <h6 class="sub-text">Home</h6>
            </div>
            <div class="w-25 text-center text-secondary">
              <i class="fa-solid fa-calendar-days"></i> <br>
              <h6 class="sub-text">Attedance</h6>
            </div>
            <div class="w-25 text-center text-danger" style="margin-top:-20px" >
              <i class="fa-solid fa-circle text-danger fa-2x "></i>
              <h6 class="sub-text mt-2">Checkout</h6>
            </div>
            <div class="w-25 text-center text-secondary">
              <i class="fa-solid fa-book"></i> <br>
              <h6 class="sub-text">Form</h6>
            </div>
            <div class="w-25 text-center text-secondary">
              <i class="fa-solid fa-gear"></i> <br>
              <h6 class="sub-text">Setting</h6>
            </div>
          </div>
        </b-navbar>
    </div>
    
    <div class="col-12 my-3 d-flex justify-content-between align-items-center">
      <h2 class="text-danger fw-bold">KerjaYuk!</h2>
      <div>
        <a href="" @click.prevent="showNotif"><i class="fa-regular text-dark fa-bell fa-2x"></i></a>
        
      </div>
    </div>
    <div class="col-12">
      <p>Hi, Good Morning!</p>
    </div>
    <!-- Humberger menu -->
    <div class="col-12">
      <div class="card p-3 rounded-card bg-profile text-white">
          <div class="d-flex justify-content-between">
            <div class="d-flex align-items">
              <b-img-lazy v-bind="mainProps" :src="getImageUrl(94)" alt="Image 8" rounded="circle"></b-img-lazy>
              <div class="title mx-2">
                <span class="profile-name">Tabay</span>
                <p class="sub-text">UI/UX Designer</p>
              </div>
            </div>
              <div class="desc">
                <span class="sub-text">Member since</span>
                <h4 class="profile-name">01 June 2021</h4>
              </div>
          </div>

          <div class="col-12">
            <span class="sub-text" style="font-style: italic;">Location</span>
          </div>

          <div class="d-flex pb-0 justify-content-between align-items-center">
            <h4 class="profile-name">Kantor Sahid</h4>
            <p class="sub-text" style="font-style:italic !important;">ICO</p>
          </div>
      </div>
    </div>

    <!-- main menu 1 -->
    <div class="col-12 mt-4 mb-4">
      <h4 class="profile-name ">Today's Activity</h4>
    </div>
    <div class="row justify-content-center">
      <div class="col-4 text-center">
          <i class="fa-regular fa-clock fa-2x text-danger "></i>
          <h5 class="mt-2 profile-name">08:30</h5>
          <h6 class="text-secondary sub-text">Check In</h6>
      </div>
      <div class="col-4 text-center">
          <i class="fas fa-sync-alt fa-2x text-danger "></i>
          <h5 class="mt-2 text-danger profile-name">03:00:00</h5>
          <h6 class="text-secondary sub-text">Working Hours</h6>
      </div>

      <div class="col-4 text-center">
          <i class="fa-solid fa-clock fa-2x text-danger "></i>
          <h5 class="mt-2 text-dark profile-name">--:--</h5>
          <h6 class="text-secondary sub-text">Check Out</h6>
      </div>
    </div>

    <!-- Main menu 2 -->
    <div class="col-12 mt-2">
      <h4 class="profile-name">PCS News</h4>
    </div>
    <div class="row justify-content-center">
    <div class="col-xl-12 col-md-12 col-sm-12 ">
        <VueSlickCarousel v-bind="settings">
            <div class="" v-for="(item, index) in items" :key="index">
              <div class="card rounded-card">
                <div class="card-body">
                <div class=" d-flex justify-content-between align-items-center">
                  <div class="d-flex align-items-center">
                    <b-img v-bind="mainProps2" rounded="circle" alt="Circle image"></b-img>
                    <h6 class="px-1 pt-2 fw-bold text-danger profile-name2">Anna Rismawati</h6>
                  </div>
                  <div class="desc">
                    <h6 class="sub-text">Senin</h6>
                    <h6 class="sub-text">30 Mei 2024</h6>
                  </div>
                </div>
                <div class="mt-2">
                  <p class="detail-content-text"> 1.lorem ipsum lorem ipsum lorem ipsum lorem </p>
                  <p class="detail-content-text"> 2.lorem ipsum lorem ipsum lorem ipsum lorem </p>
                  <p class="detail-content-text"> 3.lorem ipsum lorem ipsum lorem ipsum lorem </p>
                </div>
                </div>
              </div>
          </div>
        </VueSlickCarousel>
      </div>
    </div>

    <!-- main 3 -->

    <div class="col-12 mt-4 mb-2 ">
      <h4 class="fw-bold profile-name">Online</h4>
    </div>
    <div class="row justify-content-center">
      <div class="col-12">
        <div class="card rounded-card">
          <div class="card-body d-flex justify-content-center " >
              <div class="profile text-center" style="img-1">
                <b-img-lazy v-bind="mainProps" :src="getImageUrl(92)" alt="Image 8" rounded="circle"></b-img-lazy>
                <p class="sub-text">dea</p>
              </div>
              <div class="profile  text-center" style="img-1">
                <b-img-lazy v-bind="mainProps" :src="getImageUrl(93)" alt="Image 8" rounded="circle"></b-img-lazy>
                <p class="sub-text">dea</p>
              </div> 
              <div class="profile  text-center" style="img-1">
                <b-img-lazy v-bind="mainProps" :src="getImageUrl(98)" alt="Image 8" rounded="circle"></b-img-lazy>
                <p class="sub-text">dea</p>
              </div> 
              <div class="profile  text-center" style="img-1">
                <b-img-lazy v-bind="mainProps" :src="getImageUrl(96)" alt="Image 8" rounded="circle"></b-img-lazy>
                <p class="sub-text">dea</p>
              </div>

          </div>
        </div>
      </div>
    </div>

    <div class="mb-5"></div>
    <div class="mb-5"></div>


  </div>
</div>
    
</template>

<script>


import VueSlickCarousel from 'vue-slick-carousel';
import 'vue-slick-carousel/dist/vue-slick-carousel.css'
  // optional style for arrows & dots
  import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'

export default {
  name: 'ComponentHome',
  data() {
    return {
      mainProps: { blank: true, blankColor: '#777', width: 40, height: 40, class: 'm1' },
      mainProps2: { blank: true, blankColor: '#777', width: 24, height: 24, class: 'm1' },
      
      settings: {
        "dots": true,
        "focusOnSelect": true,
        "infinite": true,
        "speed": 500,
        "slidesToShow": 1,
        "slidesToScroll": 3,
        "touchThreshold": 5
      },
      items: [1,2,3]
    
    }
  },
  components: {
    VueSlickCarousel,
  },
  methods: {
    showNotif() {
      this.$emit('showNotif')
    },
    getImageUrl(imageId) {
      const { width, height } = this.mainProps
      return `https://picsum.photos/${width}/${height}/?image=${imageId}`
    }
  },
}
</script>

<style scoped>

.bg-profile {
  background-color: red; /* For browsers that do not support gradients */
  background-image: linear-gradient(to right, red , purple);
}

.rounded-card {
  border-radius: 16px !important; /* Sesuaikan sesuai dengan preferensi Anda */
}

.profile-name{
    font-size: 1.5vw;  
    font-weight: bold;
}
.profile-name2{
  font-size: 1.4vw;  
  font-weight: bold;
}
.sub-text{
  font-size: 1vw;
  
}

.detail-content-text{
  font-size: 1.4vw; 
  line-height: 1.2px;
  text-align: center;
}







.container {
  width: 100%; 
  margin: 0 auto; 
}

 .menu-checkout{
    position: absolute;
  }


/* Untuk perangkat seluler dengan lebar maksimum 768px */
@media (max-width: 768px) {
  .container {
    width: 92% !important; /* Mengurangi lebar kontainer untuk tampilan seluler */
  }
  .profile-name{
    font-size: 4vw;  
    font-weight: bold;
  }
  .profile-name2{
    font-size: 2.8vw;  
    font-weight: bold;
  }
  .sub-text{
    font-size: 2.6vw;
    
  }

  .detail-content-text{
    font-size: 2.8vw; 
    line-height: 1px;
  }

  

  /* Atur tata letak lainnya sesuai kebutuhan untuk tampilan seluler */
}


/* Untuk tablet dengan lebar maksimum 1024px */
@media (max-width: 1024px) {
  .container {
    width: 80%; /* Mengurangi lebar kontainer untuk tampilan tablet */
  }
    .profile-name{
    font-size: 4vw;  
    font-weight: bold;
  }
  .profile-name2{
    font-size: 2.8vw;  
    font-weight: bold;
  }
  .sub-text{
    font-size: 2.6vw;
    
  }

  .detail-content-text{
    font-size: 2.8vw; 
    line-height: 1px;
  }

 

  /* Atur tata letak lainnya sesuai kebutuhan untuk tampilan tablet */
}

</style>