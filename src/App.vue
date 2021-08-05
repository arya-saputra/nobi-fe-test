<template>
  <div id="app">
    <n-header/>
    <section class="main-section section-blue">
      <b-container>
        <b-row class="reverse">
          <b-col
            md="9">
            <h3
              class="f45">Grow Crypto The Easy Way</h3>

            <p class="mt-4 mb-4 lead">Automate your crypto trading strategy and take your emotion
              out of the equation</p>

            <div class="is-desktop">
              <div class="d-flex w-30 mt-5 justify-content-between align-items-center">
                <div class="col-6">
                  <img src="@/assets/image/a_store.svg"
                    width="90%"
                    alt="Responsive image"/>
                </div>
                <div class="col-6">
                  <img src="@/assets/image/g_play.svg"
                    width="90%"
                    alt="Responsive image"/>
                </div>
              </div>
            </div>
          </b-col>
          <b-col
            cols="3">
            <img
              class="is-desktop go-float"
              src="@/assets/image/Ilust-1-update.svg"
              width="100%">
            <img
              class="is-mobile go-float"
              src="@/assets/image/Ilust-1-update.svg"
              width="50%">
          </b-col>
        </b-row>

        <div class="is-mobile">
          <b-row class="justify-content-center">
            <b-col 
              cols="5">
              <img src="@/assets/image/a_store.svg"
                class="w-100"
                alt="Responsive image"/>
            </b-col>
            <b-col
              cols="5">
              <img src="@/assets/image/g_play.svg"
                class="w-100"
                alt="Responsive image"/>
            </b-col>
          </b-row>
        </div>
      </b-container>
    </section>
    <section class="section-black">
      <b-container>
        <b-tabs content-class="mt-5" class="n-tabs">
          <b-tab title="Strategy" class="text-white" active>
            <div class="border-black">
              <b-table
                :items="items"
                :fields="fields"
                striped
                responsive="lg">
                <template #cell(volume)="data">
                  ${{ `${addCommas(data.item.volume)}.33` }}
                </template>
                <template #cell(annual_yield)="data">
                  <div v-if="data.item.annual_yield < 0" class="text-danger">
                    {{ addCommas(data.item.annual_yield) }}%
                  </div>
                  <div v-else class="text-success">
                    +{ addCommas(data.item.annual_yield) }}%
                  </div>
                </template>
                <template #cell(node_collateral)="data">
                  <div v-if="data.item.node_collateral < 0" class="text-danger">
                    {{ addCommas(data.item.node_collateral) }}%
                  </div>
                  <div v-else class="text-success">
                    +{{ addCommas(data.item.node_collateral) }}%
                  </div>
                </template>
                <template #cell(hosted_node)="data">
                  <div v-if="data.item.hosted_node < 0" class="text-danger">
                    {{ addCommas(data.item.hosted_node) }}%
                  </div>
                  <div v-else class="text-success">
                    +{{ addCommas(data.item.hosted_node) }}%
                  </div>
                </template>
                <template #cell(month_1)="data">
                  <div v-if="data.item.month_1 < 0" class="text-danger">
                    {{ addCommas(data.item.month_1) }}%
                  </div>
                  <div v-else class="text-success">
                    +{{ addCommas(data.item.month_1) }}%
                  </div>
                </template>
                <template #cell(month_2)="data">
                  <div v-if="data.item.month_2 < 0" class="text-danger">
                    {{ addCommas(data.item.month_2) }}%
                  </div>
                  <div v-else class="text-success">
                    +{{ addCommas(data.item.month_2) }}%
                  </div>
                </template>
                <template #cell(month_3)="data">
                  <div v-if="data.item.month_3 < 0" class="text-danger">
                    {{ addCommas(data.item.month_3) }}%
                  </div>
                  <div v-else class="text-success">
                    +{{ addCommas(data.item.month_3) }}%
                  </div>
                </template>
              </b-table>
            </div>
          </b-tab>
          <b-tab title="Stacking">
            <div class="border-black">
              <b-table
                :items="items"
                :fields="fields"
                striped
                responsive="lg">
                <template #cell(volume)="data">
                  ${{ `${addCommas(data.item.volume)}.33` }}
                </template>
                <template #cell(annual_yield)="data">
                  <div v-if="data.item.annual_yield < 0" class="text-danger">
                    {{ addCommas(data.item.annual_yield) }}%
                  </div>
                  <div v-else class="text-success">
                    +{ addCommas(data.item.annual_yield) }}%
                  </div>
                </template>
                <template #cell(node_collateral)="data">
                  <div v-if="data.item.node_collateral < 0" class="text-danger">
                    {{ addCommas(data.item.node_collateral) }}%
                  </div>
                  <div v-else class="text-success">
                    +{{ addCommas(data.item.node_collateral) }}%
                  </div>
                </template>
                <template #cell(hosted_node)="data">
                  <div v-if="data.item.hosted_node < 0" class="text-danger">
                    {{ addCommas(data.item.hosted_node) }}%
                  </div>
                  <div v-else class="text-success">
                    +{{ addCommas(data.item.hosted_node) }}%
                  </div>
                </template>
                <template #cell(month_1)="data">
                  <div v-if="data.item.month_1 < 0" class="text-danger">
                    {{ addCommas(data.item.month_1) }}%
                  </div>
                  <div v-else class="text-success">
                    +{{ addCommas(data.item.month_1) }}%
                  </div>
                </template>
                <template #cell(month_2)="data">
                  <div v-if="data.item.month_2 < 0" class="text-danger">
                    {{ addCommas(data.item.month_2) }}%
                  </div>
                  <div v-else class="text-success">
                    +{{ addCommas(data.item.month_2) }}%
                  </div>
                </template>
                <template #cell(month_3)="data">
                  <div v-if="data.item.month_3 < 0" class="text-danger">
                    {{ addCommas(data.item.month_3) }}%
                  </div>
                  <div v-else class="text-success">
                    +{{ addCommas(data.item.month_3) }}%
                  </div>
                </template>
              </b-table>
            </div>
          </b-tab>
          <b-tab title="Saving">
            <div class="border-black">
              <b-table
                :items="items"
                :fields="fields"
                striped
                responsive="lg">
                <template #cell(volume)="data">
                  ${{ `${addCommas(data.item.volume)}.33` }}
                </template>
                <template #cell(annual_yield)="data">
                  <div v-if="data.item.annual_yield < 0" class="text-danger">
                    {{ addCommas(data.item.annual_yield) }}%
                  </div>
                  <div v-else class="text-success">
                    +{ addCommas(data.item.annual_yield) }}%
                  </div>
                </template>
                <template #cell(node_collateral)="data">
                  <div v-if="data.item.node_collateral < 0" class="text-danger">
                    {{ addCommas(data.item.node_collateral) }}%
                  </div>
                  <div v-else class="text-success">
                    +{{ addCommas(data.item.node_collateral) }}%
                  </div>
                </template>
                <template #cell(hosted_node)="data">
                  <div v-if="data.item.hosted_node < 0" class="text-danger">
                    {{ addCommas(data.item.hosted_node) }}%
                  </div>
                  <div v-else class="text-success">
                    +{{ addCommas(data.item.hosted_node) }}%
                  </div>
                </template>
                <template #cell(month_1)="data">
                  <div v-if="data.item.month_1 < 0" class="text-danger">
                    {{ addCommas(data.item.month_1) }}%
                  </div>
                  <div v-else class="text-success">
                    +{{ addCommas(data.item.month_1) }}%
                  </div>
                </template>
                <template #cell(month_2)="data">
                  <div v-if="data.item.month_2 < 0" class="text-danger">
                    {{ addCommas(data.item.month_2) }}%
                  </div>
                  <div v-else class="text-success">
                    +{{ addCommas(data.item.month_2) }}%
                  </div>
                </template>
                <template #cell(month_3)="data">
                  <div v-if="data.item.month_3 < 0" class="text-danger">
                    {{ addCommas(data.item.month_3) }}%
                  </div>
                  <div v-else class="text-success">
                    +{{ addCommas(data.item.month_3) }}%
                  </div>
                </template>
              </b-table>
            </div>
          </b-tab>
        </b-tabs>
        <div class="mt-5 d-flex w-100 justify-content-center">
          <b-button variant="primary" size="lg">
            <span class="mr-3">Explore More</span>
            <span class="mr-1">|</span>
            <b-icon icon="arrow-right" variant="light"></b-icon>

          </b-button>
        </div>
      </b-container>
    </section>
    <section class="section-white">
      <b-container class=" text-dark p-5">
        <b-row class="justify-content-between">
          <b-col
            sm="12"
            md="3">
            <img
              class="go-float"
              src="@/assets/image/ilust-3-update.svg"
              width="100%">
          </b-col>
          <b-col
            sm="12"
            md="8">
            <div class="font-weight-bold f45">
              <strong> Create Your Own Strategy And Become a Strategy Maker </strong>
            </div>
            <b-button class="mt-5" variant="primary" size="lg">
              <span class="mr-3">Explore More</span>
              <span class="mr-1">|</span>
              <b-icon icon="arrow-right" variant="light"></b-icon>

            </b-button>
          </b-col>
        </b-row>
      </b-container>
    </section>
    <section class="section-black">
      <b-container>
        <b-row class="justify-content-center">
          <b-col
            sm="12"
            md="12">
            <div class="font-weight-bold f45">
              <strong> Growing Crypto Has Never Been This Easy! </strong>
            </div>
            <p class="lead mt-3">NOBI makes it safe and easy to trade with our Robo Trading! Just choose the available strategy and let our startegy makers do the magic for you.</p>
          </b-col>

          <b-col
            sm="12"
            md="3"
            class="mt-3 text-center is-desktop">
            <img
              src="@/assets/image/number1-grow.svg"
              width="70%"/>
            <h4>Download App</h4>
          </b-col>
          <b-col
            sm="12"
            md="1"
            class="mt-3 d-flex justify-content-center align-items-center text-center is-desktop">
            <b-icon
              icon="arrow-right"
              class="f45 is-desktop"
              variant="light"></b-icon>
          </b-col>
          <b-col
            sm="12"
            md="3"
            class="mt-3 text-center  is-desktop">
            <img
              src="@/assets/image/number2-grow.svg"
              width="70%"/>
            <h4>Fund Your Wallet</h4>
          </b-col>
          <b-col
            sm="12"
            md="1"
            class="mt-3 d-flex justify-content-center align-items-center text-center ">
            <b-icon
              icon="arrow-right"
              class="f45  is-desktop"
              variant="light"></b-icon>
          </b-col>
          <b-col
            sm="12"
            md="3"
            class="mt-3 text-center is-desktop">
            <img
              src="@/assets/image/number3-grow.svg"
              width="70%"/>
            <h4>Start Following Strategy</h4>
          </b-col>

          <div class="is-mobile margin-center">
            <b-row class="text-left align-items-center">
              <b-col cols="4">
                <img
                src="@/assets/image/number1-grow.svg"
                width="100%"/>
              </b-col>
              <b-col cols="8">

                <h4>Download App</h4>
              </b-col>
            </b-row>
            <b-row class="text-left align-items-center">
              <b-col cols="4">
                <img
                src="@/assets/image/number2-grow.svg"
                width="100%"/>
              </b-col>
              <b-col cols="8">

                <h4>Fund Your Wallet</h4>
              </b-col>
            </b-row>
            <b-row class="text-left align-items-center">
              <b-col cols="4">
                <img
                src="@/assets/image/number3-grow.svg"
                width="100%"/>
              </b-col>
              <b-col cols="8">

                <h4>Start Following Strategy</h4>
              </b-col>
            </b-row>
          </div>
        </b-row>
      </b-container>
    </section>
    <section class="section-primary bg-primary">
      <b-container>
        <b-row class="justify-content-between">
          <b-col
            sm="12"
            md="4">
            <img class="go-float" src="@/assets/image/ilust-4-update.svg" width="70%">
          </b-col>
          <b-col
            sm="12"
            md="8"
            class="d-flex align-items-center">
            <div>
              <div class="f45 font-weight-bold">
                <strong> Start With as Little as ฿0.01</strong>
              </div>
              <p class="mt-4 text-bold font-weight-bold">You can start growing your bitcoin and other cryptocurrencies from as low as ฿0.01. Trade better by following our Trading Strategy. Our technology will help you minimize risks and enhance your gain. Simply choose & follow!</p>
            </div>
          </b-col>
        </b-row>
      </b-container>
      <div class="is-mobile">
        <b-row class="justify-content-center">
          <b-col 
            cols="5">
            <img src="@/assets/image/a_store.svg"
              class="w-100"
              alt="Responsive image"/>
          </b-col>
          <b-col
            cols="5">
            <img src="@/assets/image/g_play.svg"
              class="w-100"
              alt="Responsive image"/>
          </b-col>
        </b-row>
      </div>
    </section>
    <section class="section-white  padding-lg">
      <b-container class="is-desktop">
        <b-row>
          <b-col cols="12">
            <div class="f45 text-center mb-3">
              <strong>Powered By Industry Best</strong>
            </div>
          </b-col>
        </b-row>
        <b-row class="align-items-center justify-content-between">
          <b-col
            sm="12"
            md="2">
            <img
              src="@/assets/image/binance-logo-v2-alt.png"
              width="100%"/>
          </b-col>
          <b-col
            sm="12"
            md="2">
            <img
              src="@/assets/image/bitmex-logo-v2-alt.png"
              width="100%"/>
          </b-col>
          <b-col
            sm="12"
            md="2">
            <img
              src="@/assets/image/abi-logo-v2-alt.png"
              width="100%"/>
          </b-col>
          <b-col
            sm="12"
            md="2">
            <img
              src="@/assets/image/aave-logo-v2-alt.png"
              width="100%"/>
          </b-col>
          <b-col
            sm="12"
            md="2">
            <img
              src="@/assets/image/compound-logo-v2-alt.png"
              width="100%"/>
          </b-col>
        </b-row>
      </b-container>
      <div class="is-mobile">
        <div class="f45 text-center mb-3">
          <strong>Powered By Industry Best</strong>
        </div>
        <b-carousel
          id="carousel-fade"
          style="text-shadow: 0px 0px 2px #000"
          fade
          indicators
          interval="5000"
        >
          <b-carousel-slide
            :img-src="client_img1"
          ></b-carousel-slide>
          <b-carousel-slide
            :img-src="client_img2"
          ></b-carousel-slide>
          <b-carousel-slide
            :img-src="client_img3"
          ></b-carousel-slide>
          <b-carousel-slide
            :img-src="client_img4"
          ></b-carousel-slide>
          <b-carousel-slide
            :img-src="client_img5"
          ></b-carousel-slide>
        </b-carousel>
      </div>
    </section>
    <section class="section-navy text-center">
      <b-container>
        <b-row>
          <b-col cols="12">
            <div class="f45 text-center mb-3">
              <strong>So, what are you waiting for?</strong>
            </div>
            <p class="lead">Start Growing your Crypto and join countless crypto believers who have successfully grow with us!</p>
          </b-col>
        </b-row>
        <b-row class="align-items-center justify-content-center">
          <b-col
            md="4"
            sm="12"
            class="is-desktop mt-4">
            <b-row>
              <div class="col-6">
                <img src="@/assets/image/a_store.svg"
                  width="90%"
                  alt="Responsive image"/>
              </div>
              <div class="col-6">
                <img src="@/assets/image/g_play.svg"
                  width="90%"
                  alt="Responsive image"/>
              </div>
            </b-row>
          </b-col>
          <div class="is-mobile">
            <b-row class="justify-content-center">
              <b-col 
                cols="5">
                <img src="@/assets/image/a_store.svg"
                  class="w-100"
                  alt="Responsive image"/>
              </b-col>
              <b-col
                cols="5">
                <img src="@/assets/image/g_play.svg"
                  class="w-100"
                  alt="Responsive image"/>
              </b-col>
            </b-row>
          </div>
        </b-row>
        <p class="mt-5 w-75 margin-center">Risk warning: NOBI product offerings are subject to high market risk. Yield and return changes everytime and not guaranteed.
The volatile and unpredictable nature of the price of cryptocurrencies may result in significant loss.</p>
      </b-container>
    </section>
    <n-footer/>
  </div>
</template>

<script>
import nHeader from '@/components/nHeader.vue'
import nFooter from '@/components/nFooter.vue'

export default {
  name: 'App',
  components: {
    nHeader,
    nFooter,
  },
  data() {
    return {
      fields: [
        // A column that needs custom formatting
        { key: 'startegy', label: 'Strategy' },
        { key: 'marketcap', label: 'Marketcap' },
        { key: 'volume', label: 'Volume' },
        { key: 'annual_yield', label: 'Est Annual Yield' },
        { key: 'node_collateral', label: 'Node Collateral' },
        { key: 'hosted_node', label: 'Hosted Node' },
        // A virtual column made up from two fields
        { key: 'month_1', label: '1 Month' },
        { key: 'month_2', label: '' },
        { key: 'month_3', label: '' },
      ],
      items: [
        {
          startegy: 'DASH',
          marketcap: 'Nova Kapital',
          volume: 148574,
          annual_yield: -12.45,
          node_collateral: -2.12,
          hosted_node: -212.3,
          month_1: 212.3,
          month_2: 212.3,
          month_3: 212.3,
        },
        {
          startegy: 'SMART',
          marketcap: 'Nova Kapital',
          volume: 148574,
          annual_yield: -12.45,
          node_collateral: -2.12,
          hosted_node: 212.3,
          month_1: 212.3,
          month_2: 212.3,
          month_3: 212.3,
        },
         {
          startegy: 'ZCOIN',
          marketcap: 'Nova Kapital',
          volume: 148574,
          annual_yield: -12.45,
          node_collateral: -2.12,
          hosted_node: 212.3,
          month_1: 212.3,
          month_2: 212.3,
          month_3: 212.3,
        },
         {
          startegy: 'Nova Obscura',
          marketcap: 'Nova Kapital',
          volume: 148574,
          annual_yield: -12.45,
          node_collateral: -2.12,
          hosted_node: 212.3,
          month_1: 212.3,
          month_2: 212.3,
          month_3: 212.3,
        },
         {
          startegy: 'Neu Oscillator',
          marketcap: 'Nova Kapital',
          volume: 148574,
          annual_yield: -12.45,
          node_collateral: -2.12,
          hosted_node: -212.3,
          month_1: 212.3,
          month_2: 212.3,
          month_3: 212.3,
        },
      ],
    }
  },
  head() {
    return{
      title: 'NOBI - Grow Crypto in Easiest Way '
    }
  },
  computed: {
    client_img1() {
      return require('@/assets/image/binance-logo-v2-alt.png')
    },
    client_img2() {
      return require('@/assets/image/abi-logo-v2-alt.png')
    },
    client_img3() {
      return require('@/assets/image/bitmex-logo-v2-alt.png')
    },
    client_img4() {
      return require('@/assets/image/aave-logo-v2-alt.png')
    },
    client_img5() {
      return require('@/assets/image/compound-logo-v2-alt.png')
    },
  },
  methods: {
    addCommas(nStr) {
      nStr += '';
      const x = nStr.split('.');
      let x1 = x[0];
      let x2 = x.length > 1 ? '.' + x[1] : '';
      const rgx = /(\d+)(\d{3})/;
      while (rgx.test(x1)) {
        x1 = x1.replace(rgx, '$1' + ',' + '$2');
      }
      return x1 + x2;
    },
  }
}
</script>
