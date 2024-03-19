<template>
  <div class="col-lg-4 col-md-4 col-sm-12 col-xs-12">
    <q-card class="my-card no-shadow" bordered>
      <q-img
        src="https://cdn.quasar.dev/img/parallax1.jpg"
        basic
      >
        <div class="absolute-bottom-left bg-transparent q-ml-md">
          <div class="text-h1">
            28 <sup>o</sup>
          </div>
          <div class="text-h5">
            India
          </div>
        </div>
      </q-img>
    </q-card>
     <q-card class="fit no-shadow" bordered>
      <q-card-section class="text-h6 q-pb-none">
        <q-item>
          <q-item-section avatar class="">
            <q-icon color="blue" name="access_time" style="font-size: 2em;"/>
          </q-item-section>

          <q-item-section>
            <div class="text-h6">Booking List</div>
          </q-item-section>
        </q-item>
      </q-card-section>
      <q-card-section class="">
        <q-timeline :layout="layout" :side="side" color="secondary">

          <q-timeline-entry
            v-for="(timeline, index) in timeline_list"
            :key="index"
            :title="timeline.title"
            :subtitle="timeline.subtitle" :color="timeline.color" :icon="timeline.icon"
            :side="timeline.side"
          >
            <div style="color:gray">
              {{ timeline.desc }}
            </div>
          </q-timeline-entry>
        </q-timeline>
      </q-card-section>
    </q-card>
  </div>
</template>

<script>
import {defineComponent} from 'vue'

export default defineComponent({
  name: 'CardWithImage',
 setup() {
    return {
      timeline_list: [
        {
          title: 'Wade Woman',
          side: 'left',
          desc: '#sgl ,0 Guest',
          icon: "people"
        }
      ],
    }
  }
})
</script>
