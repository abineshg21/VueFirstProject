<template>
  <div class="col-lg-4 col-md-4 col-sm-12 col-xs-12">
   
  </div>
</template>

<script>
import {defineComponent} from 'vue'


export default defineComponent({
  name: 'CardTimeLine',
  setup() {
    return {
      timeline_list: [
        {
          title: 'Pratik Likes your product ',
          side: 'left',
          desc: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore\n' +
            '                  et dolore magna aliqua.',
          color: "red",
          icon: "thumb_up"
        },
        {
          title: 'Product Update',
          side: 'left',
          desc: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore\n' +
            '                  et dolore magna aliqua.',
          color: "orange",
          icon: "done_all"
        }, {
          title: 'Jeff Likes your product ',
          side: 'left',
          desc: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore\n' +
            '                  et dolore magna aliqua.',
          color: "blue",
          icon: "thumb_up"
        }
      ],
    }
  }
})
</script>
