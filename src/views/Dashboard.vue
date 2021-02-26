<template>
  <div id="app">
    <div class="wrapper">
      <!-- Sidebar  -->
      <nav id="sidebar">
        <div class="sidebar-header">
          <div class="px-3 py-2">
            <b-img
              center
              src="https://picsum.photos/150/150/?image=54"
              rounded="circle"
              alt="Circle image Center image"
              fluid
            ></b-img>
          </div>
          <!-- <img
            src="https://picsum.photos/200/145/?image=54"
            class="mx-auto d-block"
            width="200"
            height="145"
          /> -->
        </div>

        <ul class="list-unstyled components">
          <li>
            <router-link to="/" active-class="menuActive" exact>
              <b-icon-columns-gap
                style="width: 25px; height: 25px"
                class="align-middle mr-3"
              ></b-icon-columns-gap
              >Dashboard
            </router-link>
          </li>
          <li>
            <router-link to="/team" active-class="menuActive">
              <b-icon-calendar4-event
                style="width: 25px; height: 25px"
                class="align-middle mr-3"
              ></b-icon-calendar4-event
              >Time
            </router-link>
          </li>
        </ul>
      </nav>
      <b-container fluid class="p-0 m-0">
        <!-- Page Content  -->
        <div id="content">
          <!-- navbar -->
          <nav class="navbar navbar-expand-lg navbar-light bg-light">
            <button
              type="button"
              id="sidebarCollapse"
              class="btn btn-outline-primary btn-sm"
            >
              <b-icon-list style="width: 20px; height: 20px"></b-icon-list>
            </button>

            <div class="navbar-nav ml-auto">
              <a class="nav-link mr-2" href="#" hidden>
                <b-icon-bell-fill
                  style="width: 20px; height: 20px"
                ></b-icon-bell-fill>
                <span class="badge badge-pill badge-danger">13</span>
              </a>
            </div>

            <div class="dropdrown">
              <a class="pr-3" data-toggle="dropdown" href="#">
                <b-icon-person-circle
                  style="width: 25px; height: 25px"
                ></b-icon-person-circle>
              </a>
              <div class="dropdown-menu dropdown-menu-right mr-3">
                <div class="dropdown-item text-center">
                  <div>
                    <b-icon-person-fill
                      style="width: 40px; height: 40px"
                    ></b-icon-person-fill>
                  </div>
                  <div>Gabriel Souza</div>
                </div>
                <div class="dropdown-divider"></div>
                <a class="dropdown-item" href="#">Perfil</a>
                <a class="dropdown-item" href="#">Ajuda</a>
                <div class="dropdown-divider"></div>
                <a class="dropdown-item" href="#">Sair</a>
              </div>
            </div>
          </nav>
          <!-- Data -->
          <!-- <router-view name="cms" /> -->
          <!--  -->
        </div>
      </b-container>
    </div>
  </div>
</template>

<script>
import $ from "jquery";
export default {
  name: "app",
  data() {
    return {
      show: false,
    };
  },
  created() {},
  mounted() {
    $(document).ready(function () {
      $("#sidebarCollapse").on("click", function () {
        $("#sidebar").toggleClass("active");
        $('[data-toggle="tooltip"]').tooltip();
      });
    });
    document.title = "Champions";
  },
  methods: {},
};
</script>