<template>
  <q-page class="q-pa-sm">


    <div class="row q-col-gutter-sm  q-py-sm">
      <tab-social/>
      <card-with-image/>
      <line-chart/>
      <card-time-line/>
    </div>

    <div class="row q-col-gutter-sm  q-pb-sm">
   


    </div>
  </q-page>
</template>

<script>
import {defineComponent,defineAsyncComponent} from 'vue'

export default defineComponent({
  name: 'PageIndex',
  components: {
    TabSocial: defineAsyncComponent(() => import('components/tabs/TabSocial.vue')),
    CardWithImage: defineAsyncComponent(() => import('components/cards/CardWithImage.vue')),
    CardTimeLine: defineAsyncComponent(() => import('components/cards/CardTimeLine.vue')),
    TodoList: defineAsyncComponent(() => import('components/list/TodoList.vue')),
    TableVisits: defineAsyncComponent(() => import('components/tables/TableVisits.vue')),
    LineChart: defineAsyncComponent(() => import('components/charts/LineChart.vue')),
  },
  setup() {
    return {
      mode: 'list',
      messages: [
        {
          id: 5,
          name: 'Pratik Patel',
          msg: ' -- I\'ll be in your neighborhood doing errands this\n' +
            '            weekend. Do you want to grab brunch?',
          avatar: 'https://avatars2.githubusercontent.com/u/34883558?s=400&v=4',
          time: '10:42 PM'
        }, {
          id: 6,
          name: 'Winfield Stapforth',
          msg: ' -- I\'ll be in your neighborhood doing errands this\n' +
            '            weekend. Do you want to grab brunch?',
          avatar: 'https://cdn.quasar.dev/img/avatar6.jpg',
          time: '11:17 AM'
        }, {
          id: 1,
          name: 'Boy',
          msg: ' -- I\'ll be in your neighborhood doing errands this\n' +
            '            weekend. Do you want to grab brunch?',
          avatar: 'https://cdn.quasar.dev/img/boy-avatar.png',
          time: '5:17 AM'
        }, {
          id: 2,
          name: 'Jeff Galbraith',
          msg: ' -- I\'ll be in your neighborhood doing errands this\n' +
            '            weekend. Do you want to grab brunch?',
          avatar: 'https://cdn.quasar.dev/team/jeff_galbraith.jpg',
          time: '5:17 AM'
        }, {
          id: 3,
          name: 'Razvan Stoenescu',
          msg: ' -- I\'ll be in your neighborhood doing errands this\n' +
            '            weekend. Do you want to grab brunch?',
          avatar: 'https://cdn.quasar.dev/team/razvan_stoenescu.jpeg',
          time: '5:17 AM'
        }
      ],
    }
  },

})
</script>
