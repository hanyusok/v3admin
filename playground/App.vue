<script setup lang="ts">
import { ref } from 'vue'
import DataTable from 'datatables.net';
import JsData from './JsData.vue';
import ReactiveDt from './Reactive.vue';

let display = ref<string>('js-data');
let tables = DataTable.tables( { visible: true, api: true } );
(tables as any).columns.adjust();

</script>

<template>
  <div>
    <h1>비대면 진료 관리자</h1>

  
    <div v-show="display === 'js-data'">
      <JsData />
    </div>    
    <div v-show="display === 'reactive'">
      <ReactiveDt />
    </div>
  </div>
</template>

<style>
</style>
