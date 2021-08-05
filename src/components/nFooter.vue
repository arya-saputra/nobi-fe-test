<template>
    <section class="section-black padding-md">
      <b-container class="is-desktop">
        <b-row>
          <b-col
            md="4"
            sm="6">
            <img
                src="@/assets/image/logo.svg"
                width="120" />

            <p class="mt-4 ">Copyright &copy; year Nobi.<br>
            All trademarks and copyrights belong<br>
            to their respective owners.</p>
          </b-col>
          <b-col
            md="4"
            sm="6"
            class=" text-center">
            <div class="d-flex justify-content-between align-items-center pt-5 w-100">
              <router-link
                class="text-light"
                to="#">
                English
              </router-link>
              <router-link
                class="text-light"
                to="#">
                Terms
              </router-link>
              <router-link
                class="text-light"
                to="#">
                Contact Us
              </router-link>
            </div>
          </b-col>
          <b-col
            md="4"
            sm="12"
            class="text-right">
            <p class="lead mt-5">Join Our Community</p>
            <div class="d-flex text-right f18 justify-content-between w-50 float-right">
              <router-link>
                  <b-icon icon="bootstrap-fill" variant="light"></b-icon>
              </router-link>
              <router-link>
                  <b-icon icon="youtube" variant="light"></b-icon>
              </router-link>
              <router-link>
                  <b-icon icon="facebook" variant="light"></b-icon>
              </router-link>
              <router-link>
                  <b-icon icon="twitter" variant="light"></b-icon>
              </router-link>
              <router-link>
                  <b-icon icon="instagram" variant="light"></b-icon>
              </router-link>
              <router-link>
                  <b-icon icon="cursor" variant="light"></b-icon>
              </router-link>
            </div>
          </b-col>
        </b-row>
      </b-container>
      <b-container class="is-mobile py-5">
        <b-row>
          <b-col
            md="12"
            sm="12">
            <img
                src="@/assets/image/logo.svg"
                width="30%" />

            <p class="mt-4 f10">Copyright &copy; year Nobi.
            All trademarks and copyrights<br>belong
            to their respective owners.</p>
          </b-col>
          <b-col
            md="4"
            sm="12"
            class="text-center">
            <p class="lead mt-3 f10">Join Our Community</p>
            <div class="d-flex text-center f18 justify-content-between w-50 margin-center">
              <router-link>
                  <b-icon icon="bootstrap-fill" variant="light"></b-icon>
              </router-link>
              <router-link>
                  <b-icon icon="youtube" variant="light"></b-icon>
              </router-link>
              <router-link>
                  <b-icon icon="facebook" variant="light"></b-icon>
              </router-link>
              <router-link>
                  <b-icon icon="twitter" variant="light"></b-icon>
              </router-link>
              <router-link>
                  <b-icon icon="instagram" variant="light"></b-icon>
              </router-link>
              <router-link>
                  <b-icon icon="cursor" variant="light"></b-icon>
              </router-link>
            </div>
          </b-col>
        </b-row>
      </b-container>
    </section>
</template>