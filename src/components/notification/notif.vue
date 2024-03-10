
<template>
<div class="container">
  <b-navbar type="light" variant="light" fixed="top">
    <div class="row px-4 py-2">
      <div class="col-12 d-flex align-items-center">
        <a href="" @click.prevent="backHome">
          <i class="fa-solid fa-arrow-left fa-1x"></i>
        </a>
        <h6 class="notif-parent-old text-danger mx-4 pt-1">
          Notification
        </h6>
      </div>
    </div>
  </b-navbar>

  <div style="margin-top:70px !important"></div>
 

  <div class="notif-comp row shadow" :class="!item.read ? 'bg-unread':''" v-for="(item, i) in notifs" :key="i">
    <div class="col-12">
      <div class="px-2 py-3">
        <div class="">
          <div class="d-flex justify-content-between" >
            <div class="relative-notif">
              <img  :src="`https://picsum.photos/50/50/?image=${50+i}`" />
              <div class="absolute-notif">
                <b-icon icon="heart-fill" variant="danger"></b-icon>
              </div>
            </div>
            <div  >
              <!-- <img  src="https://picsum.photos/50/50/?image=54" /> -->
              
              <!-- <b-icon icon="heart-fill" variant="danger" style="position: absolute; bottom:0;"></b-icon> -->
            </div>
            <div class="mid w-75">
              <h6 class="notif-parent fw-bold">Reimbursement</h6>
              <p class="sub-text">
                Lorem ipsum dolor sit amet consectetur adipisicing. 
                Lorem ipsum dolor sit amet consectetur adipisicing.
              </p>
            </div>
            <div class="sub-text text-secondary">
              Today
            </div>
          
          </div>
        </div>
      </div>
    </div>
  </div>



</div>
    
</template>

<script>


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
      items: [1,2,3],
      notifs: [
        {message : 'lorem ipsung', read: false, },
        {message : 'lorem ipsung', read: true, },
        {message : 'lorem ipsung', read: true, },
        {message : 'lorem ipsung', read: true, },
        {message : 'lorem ipsung', read: false, },
        {message : 'lorem ipsung', read: false, },
        {message : 'lorem ipsung', read: false, },
        {message : 'lorem ipsung', read: false, },
        {message : 'lorem ipsung', read: false, },
        {message : 'lorem ipsung', read: true, },
        {message : 'lorem ipsung', read: true, },
        {message : 'lorem ipsung', read: true, },
        {message : 'lorem ipsung', read: true, },
        {message : 'lorem ipsung', read: true, },
      ]
    
    }
  },

  methods: {
    showNotif() {
      this.$emit('showNotif')
    },
    getImageUrl(imageId) {
      const { width, height } = this.mainProps
      return `https://picsum.photos/${width}/${height}/?image=${imageId}`
    },
    backHome(){
      this.$emit("backHome")
    }
  },
}
</script>

<style scoped>
.relative-notif {
  position: relative;
  width: 56px !important;
  height: 56px !important;
} 

.absolute-notif {
  position: absolute;
  bottom: 0;
  right: 0;
}
.bg-profile {
  background-color: red; /* For browsers that do not support gradients */
  background-image: linear-gradient(to right, red , purple);
}
.rounded-card {
  border-radius: 16px !important; /* Sesuaikan sesuai dengan preferensi Anda */
}
.notif-parent{
  font-size: 1.5vw;  
  font-weight: bold;
}
.notif-parent2{
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
    /* Tata letak default */
.container {
  width: 100%; /* Atur lebar kontainer sesuai kebutuhan */
  margin: 0 auto; /* Atur margin menjadi auto untuk memusatkan */
}

.notif-parent-old{
  font-size: 1.2em;
}

.position-relative {
  position: relative;
}

.position-absolute {
  position: absolute;
}

.bottom-0 {
  bottom: 0;
}

.end-0 {
  right: 0;
}

.notif-comp{
  cursor: -webkit-grab; cursor: grab;
}

/* Untuk perangkat seluler dengan lebar maksimum 768px */
@media (max-width: 768px) {
  .container {
    width: 100%; /* Mengurangi lebar kontainer untuk tampilan seluler */
  }
  .notif-parent{
    font-size: 2vw;  
    font-weight: bold;
  }
  .notif-parent2{
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
    width: 100%; /* Mengurangi lebar kontainer untuk tampilan tablet */
  }
    .notif-parent{
    font-size: 2.8vw;  
    font-weight: bold;
  }
  .notif-parent2{
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

.bg-unread{
  background-color:#ADD8E6 ;
}

</style>