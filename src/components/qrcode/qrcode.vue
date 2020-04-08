<template>
  <!--  调用this.$ref."名称".init(需要生成二维码的内容)-->
  <div>
    <div
      id="qrCode"
      ref="qrCodeDiv"
    />
  </div>
</template>

<script>
import QRCode from 'qrcodejs2'
export default {
  name: 'Index',
  data() {
    return {}
  },
  methods: {
    init(text) {
      this.$refs.qrCodeDiv.innerHTML = ''
      var that = this
      var time = +new Date()
      new QRCode(this.$refs.qrCodeDiv, {
        text: text + '?time=' + time,
        width: 200,
        height: 200,
        colorDark: '#333333',
        colorLight: '#ffffff',
        correctLevel: QRCode.CorrectLevel.L
      })
    }
  }
}
</script>

<style scoped>
</style>