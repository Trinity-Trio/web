<template lang='pug'>
#works
  .box
    iframe.song(scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/494605326&color=%2300615b&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true&visual=true")
    img.loading( src="~/assets/loading.svg" alt="loading" width=200)
  .box
    iframe.song(scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/493911225&color=%2300615b&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true&visual=true")
    img.loading( src="~/assets/loading.svg" alt="loading" width=200)
  .box
    iframe.song(scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/493910787&color=%2300615b&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true&visual=true")
    img.loading( src="~/assets/loading.svg" alt="loading" width=200)
  .box
    iframe.song(scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/493910124&color=%2300615b&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true&visual=true")
    img.loading( src="~/assets/loading.svg" alt="loading" width=200)
  .box
    iframe.song(scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/493909863&color=%2300615b&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true&visual=true")
    img.loading( src="~/assets/loading.svg" alt="loading" width=200)
  .box
    iframe.song(scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/493909692&color=%2300615b&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true&visual=true")
    img.loading( src="~/assets/loading.svg" alt="loading" width=200)
  .box
    iframe.song(scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/493909566&color=%2300615b&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true&visual=true")
    img.loading( src="~/assets/loading.svg" alt="loading" width=200)
</template>

<script>
export default {
}
</script>

<style lang='sass' scoped>
  #works
    background-color:
    display: flex
    flex-wrap: wrap
    .box:nth-child(3n+1)
      background-color: #FFCC00
    .box:nth-child(3n+2)
      background-color: #e95513
    .box:nth-child(3n)
      background-color: #9A35CD
    .song
      z-index: 1
      width: 100%
      height: 100%
    .box
      display: flex
      justify-content: center
      align-items: center
      flex: 1
      min-width: 30vw
      max-width: calc(100vw / 3)
      height: calc(100vw / 3)
      @media screen and (max-width:768px)
        min-width: 45vw
        max-width: calc(100vw / 2)
        height: calc(100vw / 2)
      @media screen and (max-width:411px)
        min-width: 90vw
        max-width: 100vw
        height: 100vw
      .loading
        position: absolute
        z-index: 0
        width: 150px
        height: 150px
        animation: rotation 1s infinite ease-in-out
        @keyframes rotation
          0%
            transform: rotate(0deg)
          100%
            transform: rotate(358deg)
</style>
