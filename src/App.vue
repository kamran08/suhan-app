 <template>
  <div id="app">
    <div id="main-wrapper">
      <!-- Header -->
      <!-- <div class="_1header">
        <div class="container-fuild">
          <div class="row align-items-center">
            <div class="col-12 col-md-4 col-lg-4">
              <p class="_1header_text">
                HEAD OFFICE
                <router-link to="">1760 Wilshire Blvd., LA, CA 90025</router-link>
              </p>
            </div>
            <div class="col-12 col-md-4 col-lg-4">
              <p class="_1header_text">
                MAIL
                <router-link to="">example@example.com</router-link>
              </p>
            </div>
            <div class="col-12 col-md-4 col-lg-4">
              <p class="_1header_text _last_child">
                HEAD OFFICE
                <router-link to="">+1 310 500 7834</router-link>
              </p>
            </div>
          </div>
        </div>
      </div> -->
      <!-- Header -->

      <!-- Menu -->
      <div class="_1menu">
        <div class="container-fuild">
          <div class="row align-items-center">
            <div class="col-12 col-md-auto col-lg-auto">
              <router-link to="" class="_1menu_logo">
                <!-- <h2 style="color:var(--color2)"> -->
                  <img class="_1menu_logo_img" src="../static/img/logo.png" alt="" title="">
                <!-- </h2> -->
                
              </router-link>
            </div>

            <div class="col-12 col-md col-lg">
              <ul class="_1menu_logo_list">
                <li>
                  <a href="#" class="_1menu_logo_list_text _active">Home</a>
                </li>
                <li>
                  <a href="#1" class="_1menu_logo_list_text">Services</a>
                </li>
                <li>
                  <a href="#2" class="_1menu_logo_list_text">Contact us</a>
                </li>
              </ul>
            </div>

            <!-- <div class="col-12 col-md-auto col-lg-auto">
              <ul class="_1menu_social">
                <li>
                  <a href=""><Icon type="logo-facebook" /></a>
                </li>
                <li>
                  <a href=""><Icon type="logo-linkedin" /></a>
                </li>
                <li>
                  <a href=""><Icon type="logo-twitter" /></a>
                </li>
                <li>
                  <a href=""><Icon type="logo-youtube" /></a>
                </li>
              </ul>
            </div> -->
          </div>
        </div>
      </div>
      <!-- Menu -->

      <!-- Mobile menu -->
      <div class="_mob_menu">
        <div class="_mob_menu_logo">
          <router-link to=""><img class="_mob_menu_logo_img" src="../static/img/logo.png" alt="logo" title="logo"></router-link>
        </div>

        <div class="_mob_menu_button">
          <Icon @click="isOpen = true" class="_mob_menu_button_icon" type="md-list-box" />
        </div>
      </div>

      <div :class="isOpen == true? '_mob_menu_nav_open _mob_menu_nav' : '_mob_menu_nav'">
        <ul class="_1menu_logo_list">
          <li>
            <a  @click="isOpen = false" href="#" class="_1menu_logo_list_text _active">Home</a>
          </li>
          <li>
            <a @click="isOpen = false" href="#1" class="_1menu_logo_list_text">Services</a>
          </li>
          <li>
            <a @click="isOpen = false" href="#2" class="_1menu_logo_list_text">Contact us</a>
          </li>
        </ul>

        <p @click="isOpen = false" class="_mob_menu_nav_close"><Icon type="md-close" /></p>
      </div>
      <!-- Mobile menu -->

      <div class="_main_layout">
        <router-view></router-view>
      </div>

      <!-- Footer -->
      <div v-if="$route.path != '/messenger'" class="_log_footer">
        <ul class="_log_footer_list">
          <li>
              <router-link to="/about">About</router-link>
          </li>
          <!-- <li>
              <router-link to="/support">Support</router-link>
          </li>
          <li>
              <router-link to="/donate">Donate</router-link>
          </li> -->
          <li>
              <router-link to="/terms">Terms</router-link>
          </li>
          <li>
              <router-link to="/privacy">Privacy</router-link>
          </li>
        </ul>

        <p class="_log_footer_copy">
            Services©2023. developed by 
            <a href="">ahmedkamran265@gmail.com</a>
        </p>
      </div>
      <!-- Footer -->
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return{
      isOpen:false
    }
  },

  methods:{

  },
  
  created() {
    
  }
}
</script>