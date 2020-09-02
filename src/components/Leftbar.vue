<template>
<div class="slider">
           <VueSlickCarousel
                ref="c1"
                v-bind="settings"
                >
                <div class="wraper"  v-for='(img, i) in images' :key="i">
                        <div class="inner" :style="{ backgroundImage: `url('${img.src}')` }">

                        </div>
                </div>
        </VueSlickCarousel>
</div>
     
</template>

<script>
import VueSlickCarousel from 'vue-slick-carousel'
import 'vue-slick-carousel/dist/vue-slick-carousel.css'
// optional style for arrows & dots
import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'

export default {
name: 'Leftbar',
components: { VueSlickCarousel },
  data() {
        return{
                images: [
                {
                        src: require('../assets/village.6e96038c.png')
                },
                 {
                        src: require('../assets/statewatch.dafa6e41.png')
                },
                 {
                        src: require('../assets/peaceful.5d225d72.jpg')
                },
                 {
                        src: require('../assets/agro.8510843e.png')
                },
                 {
                        src: require('../assets/monamor.c250e2f8.jpg')
                },
                 {
                        src: require('../assets/flornoy.7fafd58b.png')
                },
                 {
                        src: require('../assets/blogger.b68f061e.png')
                },
                 {
                        src: require('../assets/youtuber.20345303.png')
                },
                 {
                        src: require('../assets/yavsotne.51995980.png')
                },
                 {
                        src: require('../assets/viv_home.cdabb410.png')
                },
                {
                        src: require('../assets/vue_crm.3880cbf7.png')
                },
                {
                        src: require('../assets/node.84cfeb70.png')
                },
                {
                        src: require('../assets/React-test.943a9d78.png')
                },        

                ],
        
                settings: {
                        slidesToShow: 1,
                        dots: true,
                        focusOnSelect:true,
                        asNavFor: null
                }
        }     
  },
  mounted(){
          this.settings.asNavFor = this.$parent.$children[1].$refs.c2
  }
}
</script>

<style>

</style>