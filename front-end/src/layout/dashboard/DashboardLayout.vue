<template>
    <div class="wrapper">
        <side-bar>
            <template slot="links">
                <sidebar-link to="/" name="XSS Payload Fires" icon="fas fa-fire" />
                <sidebar-link to="/xsspayloads" name="XSS Payloads" icon="fas fa-file-code" />
                <sidebar-link to="/settings" name="Settings" icon="fas fa-cogs" />
                <li class="nav-item mt-5">
                  <a target="_blank" href="https://twitter.com/rs_loves_bugs" class="nav-link">
                    <i class="fab fa-twitter"></i>
                    <p>@rs_loves_bugs</p>
                  </a>
                </li>
                <li class="nav-item">
                  <a target="_blank" href="https://github.com/rs-loves-bugs/xsshunter" class="nav-link">
                    <i class="fab fa-github"></i>
                    <p>On Github</p>
                  </a>
                </li>
            </template>
        </side-bar>
        <div class="main-panel">
            <top-navbar></top-navbar>
            <dashboard-content @click.native="toggleSidebar">
            </dashboard-content>
            <content-footer></content-footer>
        </div>
    </div>
</template>
<style lang="scss">
</style>
<script>
import TopNavbar from "./TopNavbar.vue";
import ContentFooter from "./ContentFooter.vue";
import DashboardContent from "./Content.vue";
import MobileMenu from "./MobileMenu";
export default {
    components: {
        TopNavbar,
        ContentFooter,
        DashboardContent,
        MobileMenu
    },
    methods: {
        toggleSidebar() {
            if (this.$sidebar.showSidebar) {
                this.$sidebar.displaySidebar(false);
            }
        }
    }
};
</script>
