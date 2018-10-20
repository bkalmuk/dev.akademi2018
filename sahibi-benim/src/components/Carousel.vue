<template>
  <div>
    <b-carousel id="carousel1"
                style="text-shadow: 1px 1px 2px #333;"
                controls
                indicators
                background="#ababab"
                :interval="4000"
                img-width="1024"
                img-height="250"
                v-model="slide"
                @sliding-start="onSlideStart"
                @sliding-end="onSlideEnd"
    >

      <b-carousel-slide img-src="https://picsum.photos/1024/250/?image=54">
        <h1>Merhaba!</h1>
        <p>Bu sayfada size gösterebileceklerimi bu kayan görüntüleri takip ederek öğrenebilirsiniz.</p>
      </b-carousel-slide>
    
      <b-carousel-slide 
        caption="Kullanıcılar ! Kıymetlimisssss.."
        text="User endpoint kullanarak görüntülediğim bir sayfam var."
        img-src="https://picsum.photos/1024/250/?image=52"
      >
      </b-carousel-slide>

      <b-carousel-slide 
        caption="Nerede yaşıyor bu insanlar çoğunlukla ?"
        text="İşte bu sorunun cevabı benim sayfamda "
        img-src="https://picsum.photos/1024/250/?image=58"
      >
      </b-carousel-slide>

      <b-carousel-slide
        caption="Kaç yaşında bu değerli kullanıcılarımız?"
        text="Kullanıcının yaşı sorulmazmış...................404 ERROR.."
      >
        <img 
          slot="img" 
          class="d-block img-fluid w-100" 
          width="1024" height="250"
          src="https://picsum.photos/1024/250/?image=55" 
          alt="image slot">
      </b-carousel-slide>
      
      <b-carousel-slide
        caption="THE END"
        text="Özellikle son espriden sonra bitmeliydi zaten artık demişsinidir. Özür dilerim."
      >
        <img 
          slot="img" 
          class="d-block img-fluid w-100" 
          width="1024" height="250"
          src="https://picsum.photos/1024/250/?image=59" 
          alt="image slot">
      </b-carousel-slide>
    </b-carousel>
  </div>
</template>

<script>
export default {
  name: 'Carousel',
  data () {
    return {
      slide: 0,
      sliding: null
    }
  },
  methods: {
    onSlideStart (slide) {
      this.sliding = true
    },
    onSlideEnd (slide) {
      this.sliding = false
    }
  }
}
</script>

<style lang="scss">

</style>