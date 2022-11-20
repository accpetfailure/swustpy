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
                {list: '讨论一'},
                {list: '讨论二'}
       ]
     }
   },
   name: 'Forumindex',
   methods: {
     details () {
       this.$router.push({name: 'resources-detail'})
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
  }
</style>
