<template>
  <div class="pub_search_com">
    <div class="pub_search_wraper">
      <a href class="jump_search_page">
       <icon type="search" size="13" class="icon"></icon>
        <span>创造上海</span>
      </a>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="less" scoped>
.pub_search_com {
  background: #fff;
  width: 290px;
  height: 34px;
  margin: 0 12px;
  background: #f5f5f5;
	border-radius: 13px;
  .pub_search_wraper {
    display: flex;
    flex-wrap: nowrap;
    align-items: center;
    width: 100%;
	height: 34px;
	border-radius: 15px;
    a {
      display: block;
      width: 570rpx;
      height: 100%;
      background: #f5f5f5;
      border-radius: 15px;
      margin-right: 5px;
      display: flex;
      flex-wrap: nowrap;
      align-items: center;
      justify-content: center;
      span {
        color: #ccc;
        vertical-align: middle;
        font-size: 13px;
        margin: 0 6px;
      }
	  .icon{
		  vertical-align: middle;
		  
	  }
    }
  }
}
</style>
