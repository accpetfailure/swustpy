<template>
    <div class="box">
       <div class="value" v-for="item in ulist"><h4>{{item.list}}</h4></div>
    </div>
</template>

<script>
 export default{
   data () {
     return {
       ulist: [
                {list: '测试一'},
                {list: '测试二'}
       ]
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
