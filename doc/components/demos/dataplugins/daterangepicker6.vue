<template>
  <div>
      <p>value:{{value}}</p>
      <DateRangePicker v-model="value" :option="param"></DateRangePicker>
  </div>
</template>

<script>
import manba from 'manba';

export default {
  data() {
    return {
      value: {},
      param: {
        shortcuts:[{
          title: '近三天',
          value(){
            return {
              start: manba().add(-3, manba.DAY),
              end: manba(),
            };
          }
        }]
      }
    }
  }
}
</script>