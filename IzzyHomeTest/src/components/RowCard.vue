<script>
import Card from '../components/Card.vue';
export default {
  name:'RowCard',
  components: {
    Card,

  },
  // setup(){
  //   console.log(data);
  //   console.log(data[0]['title']);
  // }
}
</script>

<template>
    <div class="container--flex row">
        <Card/>
        <Card/>
        <Card/>
        <Card/>
    </div>
</template>
