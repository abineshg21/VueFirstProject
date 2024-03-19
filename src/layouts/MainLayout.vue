<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          @click="toggleLeftDrawer"
          aria-label="Menu"
        />
        <q-space/>
       
        <div class="q-gutter-sm row items-center no-wrap">
                <div class="bg-grey-0" style="width: 500px; padding: 5px;background-color:white">
  <q-field
    icon="wifi"
    label="Search"
    :count="10"
    helper="Some helper"
    :error="error"
    error-label="Some error"
  >
    <q-search
      v-model="text"
      dark
      inverted
      color="white"
      float-label="Textfield"
    />
  </q-field>
</div>
          <q-btn round dense flat color="black" icon="notifications">
            <q-badge color="red" text-color="white" floating>
              5
            </q-badge>
            <q-menu
            >
              <q-list style="min-width: 100px">
                <messages></messages>
                <q-card class="text-center no-shadow no-border">
                  <q-btn label="View All" style="max-width: 120px !important;" flat dense
                         class="text-indigo-8"></q-btn>
                </q-card>
              </q-list>
            </q-menu>
          </q-btn>
          <label> Backiyaraj</label>
          <q-btn round flat>
            <q-avatar size="26px">
           
              <img src="https://cdn.quasar.dev/img/boy-avatar.png">
            </q-avatar>
          </q-btn>
        </div>
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
      style="top:40px"
      class="bg-primary text-white"
    >
      <q-list  style="margin-top:40px">
       <q-item  active-class="q-item-no-link-highlighting" style="text-align:center" >
          
          <q-item-section>
            <q-item-label style="font-size:30px">Hotel SWAN</q-item-label>
          </q-item-section>
        </q-item>
        <q-item to="/" active-class="q-item-no-link-highlighting"  style="margin-top:40px">
          <q-item-section avatar>
            <q-icon name="dashboard"/>
          </q-item-section>
          <q-item-section>
            <q-item-label>OverView</q-item-label>
          </q-item-section>
        </q-item>
        <q-item to="/" active-class="q-item-no-link-highlighting">
          <q-item-section avatar>
            <q-icon name="date_range"/>
          </q-item-section>
          <q-item-section>
            <q-item-label>Calendar</q-item-label>
          </q-item-section>
        </q-item>
 <q-item to="/" active-class="q-item-no-link-highlighting">
          <q-item-section avatar>
            <q-icon name="key"/>
          </q-item-section>
          <q-item-section>
            <q-item-label>Booking</q-item-label>
          </q-item-section>
        </q-item>

 <q-item to="/" active-class="q-item-no-link-highlighting">
          <q-item-section avatar>
            <q-icon name="people"/>
          </q-item-section>
          <q-item-section>
            <q-item-label>Earning</q-item-label>
          </q-item-section>
        </q-item>

       <q-item to="/" active-class="q-item-no-link-highlighting">
          <q-item-section avatar>
            <q-icon name="people"/>
          </q-item-section>
          <q-item-section>
            <q-item-label>Staff</q-item-label>
          </q-item-section>
        </q-item>
      </q-list>
    </q-drawer>

    <q-page-container class="bg-grey-2">
      <router-view/>
    </q-page-container>
  </q-layout>
</template>

<script>
import Messages from "./Messages.vue";

import {defineComponent, ref} from 'vue'
import {useQuasar} from "quasar";

export default defineComponent({
  name: 'MainLayout',

  components: {
    Messages
  },

  setup() {
    const leftDrawerOpen = ref(false)
    const $q = useQuasar()

    return {
      $q,
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value
      }
    }
  }
})
</script>

<style>

/* FONT AWESOME GENERIC BEAT */
.fa-beat {
  animation: fa-beat 5s ease infinite;
}

@keyframes fa-beat {
  0% {
    transform: scale(1);
  }
  5% {
    transform: scale(1.25);
  }
  20% {
    transform: scale(1);
  }
  30% {
    transform: scale(1);
  }
  35% {
    transform: scale(1.25);
  }
  50% {
    transform: scale(1);
  }
  55% {
    transform: scale(1.25);
  }
  70% {
    transform: scale(1);
  }
}

</style>
