<template>
  <section class="bg-poppiesImage bg-cover w-full h-full flex justify-center items-center relative z-0">
    <div class="p-5 text-white text-center">
      <div data-aos="fade-up" data-aos-duration="1800">
        <h1 class="mb-3 md:mb-5 text-5xl md:text-6xl">Amanda & Tim</h1>
        <p class="mb-10 md:mb-14 font-light text-2xl md:text-3xl">30 juli 2022 <span>&#183;</span> Kungsberg Gård, Strängnäs</p>
        <button-white-outline buttonLink='/osa' text='OSA' />
      </div>
    </div>
  </section>
  <section class="bg-white p-5 py-10 md:py-20 lg:py-40">
    <div class="md:w-3/4 mx-auto lg:flex lg:space-x-32 text-center lg:text-left">
      <div class="hidden lg:block lg:w-1/3 text-4.5xl font-light">
        <p data-aos="fade-right">Allt du behöver veta</p>
      </div>
      <div class="lg:w-3/4 my-12 md:my-0">
        <div class="text-xl font-light">
          <div class="space-y-6 lg:mb-8">
          <p>Vi gifter oss lördagen 30 juli och hoppas att du vill vara med.</p>
          <p>Vigsel, middag och fest äger rum på Kungsberg Gård, 15 km utanför Strängnäs. All praktisk info om och inför dagen hittar på den här sidan.</p>
          </div>
          <div class="hidden lg:block space-y-5">
            <p><span class="font-semibold">15:00</span> Välkommen till Kungsberg</p>
            <p><span class="font-semibold">16:00</span> Vigsel och mingel</p>
            <p><span class="font-semibold">18:00</span> Middag på magasinet</p>
            <p><span class="font-semibold">21:00</span> Fest så länge vi vill och orkar</p>
          </div>
          <button-black buttonLink='/info' text='MER INFO' class="mt-16 text-sm" />
        </div>
      </div>
    </div>
  </section>
  <contact-section />
</template>


<script>
import ButtonWhiteOutline from '../components/buttons/ButtonWhiteOutline.vue';
import ButtonBlack from '../components/buttons/ButtonBlack.vue';
import ContactSection from '../components/sections/ContactSection.vue'

export default {
  components: { ButtonWhiteOutline, ButtonBlack, ContactSection },
  name: 'Home',
  computed: {
    navLight() {
      return this.$store.state.navLight
    }
  },
  mounted () {
    this.$store.commit('toggleNavTheme', true)
  }
}
</script>