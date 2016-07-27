<template>
  <div id="app">
    <h1>vue分页</h1>
    <pagination :count="count" :page="page" :show-size="showSize" :page-size="pageSize"></pagination>
  </div>
</template>

<script>
import Pagination from './components/pagination.vue';
export default {
  data () {
    return {
      count:300,
      page:1,      
      showSize:10,
      pageSize:20
    }
  },
  components:{
    Pagination
  },
  events:{
    onChangePage(page){
      console.log(page);
    }
  }
}
</script>

<style>
body {
  font-family: Helvetica, sans-serif;
}
.pagination{
  padding:0;
  margin:0;
  list-style:none;
  font-size:0;
}
.pagination li{
  display:inline-block;
  padding:4px 8px;
  border:1px solid #ddd;  
  margin-left:-1px;
  cursor: pointer;
}
.pagination li.active{
  background:green;
  border-color:green;
  color:#fff;
  cursor: default;
}
.pagination li >*{
  font-size:14px;
}
.pagination li a{
  display:block;
}
</style>
