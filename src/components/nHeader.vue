<template>
    <div :class="hang? 'sticky header-top':'header-top'">
        <b-container class="is-desktop">
            <b-row>
                <b-col
                   md="9"
                   sm="12">
                 <img
                   src="@/assets/image/logo.svg"
                   width="120" />
                </b-col>
                <b-col
                   md="3"
                   sm="12">
                   <b-row>
                     <b-col
                       md="6"
                       sm="12"
                       class="text-right pr-2 border-thin">
                       Strategy Maker
                     </b-col>
                     <b-col
                       md="6"
                       sm="12">
                        Blog
                     </b-col>
                   </b-row>
                </b-col>
            </b-row>
        </b-container>
        <div class="text-center is-mobile">
          <img
              src="@/assets/image/logo.svg"
              width="120" />
        </div>
    </div>
</template>
<script>
export default {
  data() {
    return {
      hang: false,
    };
  },
  mounted() {
    this.scroll();
  },
  methods: {
    isScrolledIntoView (el) {
      let rect = el.getBoundingClientRect()
      let elemTop = rect.top
      let elemBottom = rect.bottom - 500

      let isVisible = elemTop < window.innerHeight && elemBottom >= 0
      return isVisible
    },
    scroll () {
      window.onscroll = () => {
        let scrolledTo = document.querySelector('.main-section')

        if (scrolledTo && this.isScrolledIntoView(scrolledTo)) {
          this.hang = false;
        } else {
          this.hang = true;
        }
      }
    }
  }
}
</script>
<style scoped>
.header-top {
    background: black;
    padding: 20px 0;
    color: white;
}

.border-thin {
    border-right: 1px solid rgb(59, 59, 59);
}

.text-right {
    text-align: right;
}

.sticky {
  position: fixed;
  width: 100%;
  z-index: 100;
}
</style>
