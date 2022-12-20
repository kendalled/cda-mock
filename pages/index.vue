<template>
  <main>
    <Navbar />
    <AngledHero />
    <LogoCloud />

    <AltFeatures />
    <PictureStats />
    <ContentPiece />
    <Checklist />
    <SimpleAction />
    <DarkFooterTwo />
  </main>
</template>

<script>
import 'aos/dist/aos.css'
import aos from 'aos'

export default {
  mounted () {
    aos.init()
  }
}
</script>
