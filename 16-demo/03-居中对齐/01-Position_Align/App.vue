<template>
  <div id="app">
    <div class="container">
      <div id="black">
        <img
          src="https://codingstartup.com/assets/centering-elements/black.png"
          alt=""
        />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
#app {
  width: 100vw;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  .container {
    width: 200px;
    min-height: 200px;
    background: url("https://codingstartup.com/assets/centering-elements/dart.png")
      no-repeat center;
    background-size: contain;
    position: relative;
    #black {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translateX(-50%) translateY(-50%);
      img {
        width: 60px;
        height: 60px;
      }
    }
  }
}
</style>
