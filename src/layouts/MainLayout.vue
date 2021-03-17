<template>
  <q-layout view="lHh Lpr lFf">
<!--   <style
      @font-face {
      font-family: oraclefont;
      src:oraclefont.woff);
    }></style>-->
    <q-header elevated>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="leftDrawerOpen = !leftDrawerOpen"
        />
<!--        <img
          alt="oracle-logo"
          src="~icons/favicon-32x32.png"
        >-->
        <q-toolbar-title>

          <q-avatar>
            <img src="oraclelogowhite.png">
          </q-avatar>

          ORACLES.CC



        </q-toolbar-title>

<!--        <q-btn label="Get Zap" color="success" @click="alert = true" />-->

        <div>

         Powered by Zap.org and Quasar v{{ $q.version }}
        </div>
      </q-toolbar>
    </q-header>



    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
      content-class="bg-grey-1"
    >
      <q-list>
        <q-item-label
          header
          class="text-grey-8"
        >
          Navigation Bar
        </q-item-label>
        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>

<!--    <q-dialog v-model="alert" align="center"  style="min-width:450px;">
      <q-card style="min-width:450px;">
        <q-card-section>
          <div class="text-h6">Buy Zap on Uniswap</div>
        </q-card-section>

        <q-card-section>
          <iframe
            src="https://app.uniswap.org/#/swap?outputCurrency=0x6781a0f84c7e9e846dcb84a9a5bd49333067b104"
            height="660px"
            width="100%"
            style="
          border: 0;
          margin: 0 auto;
          display: block;
          border-radius: 10px;
          max-width: 800px;
          min-width: 300px;
        "
            id="myId"
          />
        </q-card-section>

        <q-card-actions align="right">
          <q-btn flat label="OK" color="primary" v-close-popup />
        </q-card-actions>
      </q-card>
    </q-dialog>-->
    <q-footer elevated>
      <q-toolbar>
        <q-toolbar-title>enterprise level oracle solutions</q-toolbar-title>
      </q-toolbar>
    </q-footer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import EssentialLink from 'components/EssentialLink.vue'

const linksData = [
  {
    title: 'Discord Channel',
    caption: 'https://discord.gg/PfcecUPbUH',
    icon: 'chat',
    link: 'https://discord.gg/PfcecUPbUH'
  },
  {
    title: 'Blog',
    caption: 'https://medium.com/@oracles.cc',
    icon: 'record_voice_over',
    link: 'https://medium.com/@oracles.cc'
  },
  {
    title: 'Zap',
    caption: 'Zap.org',
    icon: 'rss_feed',
    link: 'https://zap.org'
  }

];

export default {
  name: 'MainLayout',
  components: { EssentialLink },
  data () {
    return {
      leftDrawerOpen: false,
      essentialLinks: linksData
    }
  }
}
</script>
