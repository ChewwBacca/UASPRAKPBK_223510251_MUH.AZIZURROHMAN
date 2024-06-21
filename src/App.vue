<template>
  <q-layout view="hHh lpR fFf">
    <q-header elevated>
      <q-toolbar>
        <q-toolbar-title>
          MUH. AZIZURROHMAN
        </q-toolbar-title>
        <q-btn flat label="WEATHER CHECK" @click="goTo('/')"/>
        <q-btn flat label="TUGAS AZIZ">
          <q-menu>
            <q-list>
              <q-item clickable v-ripple @click="goTo('/tugas1')">
                <q-item-section>TUGAS 1</q-item-section>
              </q-item>
              <q-item clickable v-ripple @click="goTo('/tugas2')">
                <q-item-section>TUGAS 2</q-item-section>
              </q-item>
              <q-item clickable v-ripple @click="goTo('/tugas3')">
                <q-item-section>TUGAS 3</q-item-section>
              </q-item>
              <q-item clickable v-ripple @click="goTo('/tugas4')">
                <q-item-section>TUGAS 4</q-item-section>
              </q-item>
              <q-item clickable v-ripple @click="goTo('/tugas5')">
                <q-item-section>TUGAS 5</q-item-section>
              </q-item>
              <q-item clickable v-ripple @click="goTo('/tugas6')">
                <q-item-section>TUGAS 6</q-item-section>
              </q-item>
              <q-item clickable v-ripple @click="goTo('/tugas7')">
                <q-item-section>MATERI 7</q-item-section>
              </q-item>
            </q-list>
          </q-menu>
        </q-btn>
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view/>
    </q-page-container>

    <q-footer class="bg-grey-8 text-white">
      <div class="footer-content">
        &copy; 2024 Muh.Azizurrohman. All rights reserved.
      </div>
    </q-footer>
  </q-layout>
</template>

<script>
export default {
  methods: {
    goTo(path) {
      this.$router.push(path);
    }
  }
};
</script>

<style>
body {
  font-family: Roboto, sans-serif;
}

.footer-content {
  width: 100%;
  text-align: center;
  padding: 3px 0;
  font-size: 0.875rem; 
}
</style>
