<template>
    <div class="box">
       <div class="value" v-for="item in ulist"><button v-on:click="details">{{item.list}}</button></div>
    </div>
</template>

<script>
 export default{
   data () {
     return {
       ulist: [
                {list: '课件一'},
                {list: '课件二'}
       ]
     }
   },
   name: 'Content',
   methods: {
     details () {
       this.$router.push({name: 'resources-details-ID'})
     }
   }
}
</script>
<style  scoped>
  .value{
    border: 1px solid;
    width:900px;
    height:200px;
    margin: auto;
    margin-top: 25px;
    text-align: center;
     padding-top: 5%; 
  };
  .button::after
  {
    border: 0;
  }
</style>
