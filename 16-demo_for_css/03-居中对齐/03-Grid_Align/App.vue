<template>
  <div id="app">
    <div class="container">
      <div id="black">
        <img src="https://codingstartup.com/assets/centering-elements/black.png" alt />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
%flex-center {
  display: grid;
  justify-content: center;
  align-items: center;
}
#app {
  width: 100vw;
  min-height: 100vh;
  @extend %flex-center;
  .container {
    width: 400px;
    min-height: 400px;
    background: url("https://codingstartup.com/assets/centering-elements/dart.png")
      no-repeat center;
    background-size: contain;
    @extend %flex-center;
    #black {
      img {
        width: 60px;
        height: 60px;
      }
    }
  }
}
</style>
