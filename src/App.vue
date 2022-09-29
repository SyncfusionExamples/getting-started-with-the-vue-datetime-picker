<template>
  <div class="wrapper">
    <ejs-datetimepicker placeholder="Choose a date and time"
      :value="datetimeValue"
      :min="minDateTime"
      :max="maxDateTime"
      :enableMask="true"
      format="dd-MMM-yy HH:mm"
      step="60"></ejs-datetimepicker>
  </div>
</template>

<script>
import {DateTimePickerComponent, MaskedDateTime} from "@syncfusion/ej2-vue-calendars";

export default {
  name: 'App',
  components: {
    "ejs-datetimepicker": DateTimePickerComponent
  },
  data(){
    return{
      datetimeValue: new Date("09/23/2022 2:30 PM"),
      minDateTime: new Date("09/19/2022 9:00 AM"),
      maxDateTime: new Date("09/23/2022 6:00 PM"),
    }
  },
  provide:{
    datetimepicker: [MaskedDateTime]
  }
}
</script>

<style>
  @import '../node_modules/@syncfusion/ej2-base/styles/material.css';
  @import '../node_modules/@syncfusion/ej2-buttons/styles/material.css';
  @import '../node_modules/@syncfusion/ej2-inputs/styles/material.css';
  @import '../node_modules/@syncfusion/ej2-popups/styles/material.css';
  @import '../node_modules/@syncfusion/ej2-lists/styles/material.css';
  @import "../node_modules/@syncfusion/ej2-vue-calendars/styles/material.css";
  .wrapper{
    max-width: 250px;
    margin: 0 auto;
  }
</style>
