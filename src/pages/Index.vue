<template>
  <q-page class="flex flex-center">
    <img
      alt="geckologo"
      src="~assets/coingeckoimage.png"
    >
    <zap-bond-widget address="0xa051812253487ee89c3491AE74f57536b7046445" endpoint="Test0"></zap-bond-widget>
  </q-page>
</template>
<script>
export default {
  name: 'PageIndex',
  data () {
    return {
      coinGeckoOracle:"0xF02491e199565B9822ECf001eB6a336959D655C8",
      status:"online",
      accounts:"",
      slide: 'style',
      coingecko: 'CoinGecko is a cryptocurrency ranking website that gives a 360 degree overview of cryptocurrencies.'
    }
  }
}
</script>
