<template>
  <div
    class="offcanvas offcanvas-start"
    v-bind:class="{
      'show' : show_sidebar,
    }"
    v-bind:style="{
      'visibility' : (show_sidebar) ? 'visible' : 'hidden'
    }"
    tabindex="-1"
    id="sidebarPanel"
  >
    <div class="offcanvas-body">
      <!-- profile box -->
      <div class="profileBox">
        <div class="image-wrapper">
          <img
            src="/mobile/assets/img/logo.png"
            alt="image"
            class="imaged rounded"
          />
        </div>
        <div class="in">
          <strong>Saleman</strong>
          <div class="text-muted">
            <ion-icon
              name="location"
              role="img"
              class="md hydrated"
              aria-label="location"
            ></ion-icon>
            Nhân Viên
          </div>
        </div>
        <a href="#" id="close-sidebar" class="close-sidebar-button" @click="this.$emit('closeSidebarCallBack', {})">
          <ion-icon
            name="close"
            role="img"
            class="md hydrated"
            aria-label="close"
          ></ion-icon>
        </a>
      </div>
      <!-- * profile box -->

      <ul class="listview flush transparent no-line image-listview mt-2">
        <li>
          <router-link :to="{ name: 'home', params: {} }" class="item" active-class="active" @click="this.$emit('closeSidebarCallBack')">
            <div class="icon-box bg-warning">
              <ion-icon
                name="home-outline"
                role="img"
                class="md hydrated"
                aria-label="home outline"
              ></ion-icon>
            </div>
            <div class="in">Trang Chủ</div>
          </router-link>
        </li>
        <li>
          <router-link :to="{ name: 'products.type', params: {'product_type':'hot_products'} }" class="item" active-class="active" @click="this.$emit('closeSidebarCallBack')">
            <div class="icon-box bg-danger">
              <ion-icon
                name="ribbon-outline"
                role="img"
                class="md hydrated"
                aria-label="home outline"
              ></ion-icon>
            </div>
            <div class="in">Sản Phẩm Hot</div>
          </router-link>
        </li>
        <li>
          <router-link :to="{ name: 'products.type', params: {'product_type':'block_products'} }" class="item" active-class="active" @click="this.$emit('closeSidebarCallBack')">
            <div class="icon-box bg-success">
              <ion-icon
                name="storefront-outline"
                role="img"
                class="md hydrated"
                aria-label="home outline"
              ></ion-icon>
            </div>
            <div class="in">Sản Phẩm Block</div>
          </router-link>
        </li>
        <li>
          <router-link :to="{ name: 'products.type', params: {'product_type':'delivery_products'} }" class="item" active-class="active" @click="this.$emit('closeSidebarCallBack')">
            <div class="icon-box bg-info">
              <ion-icon
                name="rocket-outline"
                role="img"
                class="md hydrated"
                aria-label="home outline"
              ></ion-icon>
            </div>
            <div class="in">Sản Phẩm Ký Gửi</div>
          </router-link>
        </li>
        <li>
          <router-link :to="{ name: 'products.type', params: {'product_type':'future_products'} }" class="item" active-class="active" @click="this.$emit('closeSidebarCallBack')">
            <div class="icon-box bg-dark">
              <ion-icon
                name="alarm-outline"
                role="img"
                class="md hydrated"
                aria-label="home outline"
              ></ion-icon>
            </div>
            <div class="in">Chuẩn Bị Mở Bán</div>
          </router-link>
        </li>
         <li>
          <router-link :to="{ name: 'products.type', params: {'product_type':'expired_products'} }" class="item" active-class="active" @click="this.$emit('closeSidebarCallBack')">
            <div class="icon-box bg-danger">
              <ion-icon
                name="alarm-outline"
                role="img"
                class="md hydrated"
                aria-label="home outline"
              ></ion-icon>
            </div>
            <div class="in">Hết Hạn</div>
          </router-link>
        </li>
         <li>
          <router-link :to="{ name: 'products.type', params: {'product_type':'sold_products'} }" class="item" active-class="active" @click="this.$emit('closeSidebarCallBack')">
            <div class="icon-box bg-info">
              <ion-icon
                name="alarm-outline"
                role="img"
                class="md hydrated"
                aria-label="home outline"
              ></ion-icon>
            </div>
            <div class="in">Đã Bán</div>
          </router-link>
        </li>
        <li>
          <router-link :to="{ name: 'collaborators.index', params: {} }" class="item" active-class="active" @click="this.$emit('closeSidebarCallBack')">
            <div class="icon-box bg-danger">
              <ion-icon
                name="accessibility-outline"
                role="img"
                class="md hydrated"
              ></ion-icon>
            </div>
            <div class="in">Khách Hàng</div>
          </router-link>
        </li>
        <li>
          <router-link :to="{ name: 'products.type', params: {'product_type':'quang_tri'} }" class="item" active-class="active" @click="this.$emit('closeSidebarCallBack')">
            <div class="icon-box bg-primary">
              <ion-icon
                name="pin"
                role="img"
                class="md hydrated"
              ></ion-icon>
            </div>
            <div class="in">Đất Quảng Trị</div>
          </router-link>
        </li>
        <li>
          <router-link :to="{ name: 'products.type', params: {'product_type':'quang_binh'} }" class="item" active-class="active" @click="this.$emit('closeSidebarCallBack')">
            <div class="icon-box bg-primary">
              <ion-icon
                name="pin"
                role="img"
                class="md hydrated"
              ></ion-icon>
            </div>
            <div class="in">Đất Quảng Bình</div>
          </router-link>
        </li>
        <li>
          <router-link :to="{ name: 'products.type', params: {'product_type':'hue'} }" class="item" active-class="active" @click="this.$emit('closeSidebarCallBack')">
            <div class="icon-box bg-primary">
              <ion-icon
                name="pin"
                role="img"
                class="md hydrated"
              ></ion-icon>
            </div>
            <div class="in">Đất Huế</div>
          </router-link>
        </li>
        <li>
          <router-link :to="{ name: 'products.type', params: {'product_type':'da_nang'} }" class="item" active-class="active" @click="this.$emit('closeSidebarCallBack')">
            <div class="icon-box bg-primary">
              <ion-icon
                name="pin"
                role="img"
                class="md hydrated"
              ></ion-icon>
            </div>
            <div class="in">Đất Đà Nẵng</div>
          </router-link>
        </li>
      </ul>
    </div>

  </div>

  <div class="offcanvas-backdrop fade show" v-if="show_sidebar" @click="this.$emit('closeSidebarCallBack')"></div>
</template>

<script>
export default {
  props: ["show_sidebar"],
};
</script>

<style>
</style>