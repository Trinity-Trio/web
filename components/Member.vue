<template lang='pug'>
#member
  #CHARLII_k.item(@click='charlii', :class='{active: isCha}')
    img(src='~/assets/memberCHARLII_k.svg')
    h3 CHARLII_k
    p やばいやつです。
  #ryu-g.item(@click='ryu', :class='{active: isRyu}')
    img(src='~/assets/memberryu-g.svg')
    h3 ryu-g
    p やばいやつです。
  #by_sK.item(@click='sk', :class='{active: isK}')
    img(src='~/assets/memberby_sK.svg')
    h3 by_sK
    p やばいやつです。
</template>

<script>
export default {
  data: () => {
    return {
      isCha: false,
      isRyu: false,
      isK: false
    }
  },
  methods: {
    charlii: function () {
      this.isCha = true
      this.isRyu = false
      this.isK = false
    },
    ryu: function () {
      this.isCha = false
      this.isRyu = true
      this.isK = false
    },
    sk: function () {
      this.isCha = false
      this.isRyu = false
      this.isK = true
    }
  }
}
</script>

<style lang='sass' scoped>
// pc
$cha-w: .92
$ryu-w: 1
$sk-w: .94

// sp
$cha-h: .92
$ryu-h: 1
$sk-h: .90

// too
$size: 5

#member
  height: 100vh
  display: flex
  flex-direction: row
  @media screen and ( max-width : 768px )
    flex-direction: column

#CHARLII_k
  background-color: #FFCC00
  color: #FFCC00
  flex-grow: $cha-w
  p
    background-color: #FFCC00
    color: #000
  @media screen and ( max-width : 768px )
    flex-grow: $cha-h
  &.active
    @extend .active
    flex-grow: $cha-w * $size
    @media screen and ( max-width : 768px )
      flex-grow: $cha-h * $size
    &:hover
      img
#ryu-g
  background-color: #E95513
  color: #E95513
  flex-grow: $ryu-w
  p
    background-color: #E95513
    color: #000
  @media screen and ( max-width : 768px )
    flex-grow: $ryu-h
  &.active
    @extend .active
    flex-grow: $ryu-w * $size
    @media screen and ( max-width : 768px )
      flex-grow: $ryu-h * $size
    &:hover
      img
#by_sK
  background-color: lighten(#4e1a68, 25%)
  color: lighten(#4e1a68, 25%)
  flex-grow: $sk-w
  p
    background-color: lighten(#4e1a68, 25%)
    color: #000
  @media screen and ( max-width : 768px )
    flex-grow: $sk-h
  &.active
    @extend .active
    flex-grow: $sk-w * $size
    @media screen and ( max-width : 768px )
      flex-grow: $sk-h * $size
    &:hover
      img

.active
  img
    left: 0
  p
    display: block
    position: absolute
    top: 50%
    left: 50%
    z-index: 100

.item
  position: relative
  // text-align: center
  overflow: hidden
  transition: .2s
  img
    position: absolute
    bottom: -1rem
    height: 100vh
    left: 50%
    right: 50%
    transform: translateX(-50%)
    z-index: 1
    transition: .2s
    @media screen and ( max-width : 768px )
      transition: none
      top: -70vh
      bottom: auto
      height: 220vh
      left: 25%
  h3
    position: absolute
    left: 2rem
    bottom: 2rem
    z-index: 2
    font-size: 1.5rem
    font-weight: bold
    background-color: #000
    padding: 0 .2em .2em
    height: 1em
    @media screen and ( max-width : 768px )
      left: 1rem
      top: 1rem
      font-size: 1.2rem
  p
    display: none
  &:hover
    img
      bottom: 0rem
</style>
