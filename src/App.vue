<template >
  <div class="container">
    <div class="wrapper">
      <button-nav @action="setIndex" />
  
    <!-- INFO -->
     <component :is="activeComp[activeIndex]" @setModel="setModel"></component>
     <Modal v-if="isOpen" :imgge="modalImage" @closeModel="isOpen = false"/>
    </div>
  </div>
</template>


<script>

import ButtonNav from './components/Button-nav.vue'
import AboutUs from './components/About-us.vue'
import Team from './components/Team.vue'
import Cert from './components/Cert.vue'
import Modal from './components/Modal.vue'

export default {
  
  components: { ButtonNav, AboutUs, Team, Cert, Modal},


  data(){
    return {
      isOpen: false,
      modalImage: 0,
      activeIndex: 0,
      activeComp: [
        'AboutUs',
        'Team',
        'Cert',
        
      ],
      aboutData: [
        {
          btnName: 'About us'
        },
        {
          btnName: 'Our team'
        },
        {
          btnName: 'Certificates'
        }                     
      ]
    }
  },

  provide() {
    return {
      btnInfo: this.aboutData
    }
  },

  methods: {
      setIndex(idx){
        this.activeIndex = idx  
      },
      setModel(img){
          this.modalImage = img
          this.isOpen = true
      }
  }  
  
}
</script>


<style lang="scss">
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  button {
    outline: none;
    cursor: pointer;
    background: none;

  }

  body{
    font-family:'Gill Sans',  sans-serif;
    color: #333;
    font-size: 18px;
    font-weight: 400;
    background: #05001b;
  }

  .container {
    width: 1110px;
    margin: 0 auto;
  }
  .red{
    color: red;
  }
</style>