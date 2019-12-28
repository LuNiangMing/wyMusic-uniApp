<template>
  <div class="found_page">
    <div class="find_page_header">
      <div class="maike left">
        <a href></a>
      </div>
      <Search/>
	  <div class="playing_audio right">
		  <a href="">
			  <uni-icon type=""></uni-icon>
		  </a>
	  </div>
    </div>
    <Carousel/>
    <!--频道选择-->
    <div class="category_channel">
      <div class="category_channel_wrapper clearfix">
        <div class="no-margin-left">
          <a href>
            <img src="./imgs/tui.png" alt>
          </a>
          <span>每日推荐</span>
        </div>

        <div>
          <a href>
            <img src="./imgs/songlist.png" alt>
          </a>
          <span>歌单</span>
        </div>
        <div>
          <a href>
            <img src="./imgs/pai.png" alt>
          </a>
          <span>排行榜</span>
        </div>
        <div>
          <a href>
            <img src="./imgs/diantai.png" alt>
          </a>
          <span>电台</span>
        </div>

        <div class="no-margin-right">
          <a href>
            <img src="./imgs/zhibo.png" alt>
          </a>
          <span>直播</span>
        </div>
      </div>
    </div>
    <!--推荐歌单-->
    <div class="good_song_list clearfix">
      <div class="good_song_list_wrapper clearfix">
        <div class="songlist_header">
          <h4 class="left">推荐歌单</h4>
          <a href class="songlist-plaza right">
            <span>歌单广场</span>
          </a>
        </div>
        <div class="hot_song_con clearfix">
          <a href>
            <div class="song_img">
              <img src="./imgs/109951164569993065.jpg" alt>
            </div>
            <div class="song_text">[VIP专享]一周新歌推荐</div>
          </a>
          <a href>
            <div class="song_img">
              <img src="./imgs/109951164569993065.jpg" alt>
            </div>
            <div class="song_text">[VIP专享]一周新歌推荐</div>
          </a>
          <a href>
            <div class="song_img">
              <img src="./imgs/109951164569993065.jpg" alt>
            </div>
            <div class="song_text">[VIP专享]一周新歌推荐</div>
          </a>
          <a href>
            <div class="song_img">
              <img src="./imgs/109951164569993065.jpg" alt>
            </div>
            <div class="song_text">[VIP专享]一周新歌推荐</div>
          </a>
          <a href>
            <div class="song_img">
              <img src="./imgs/109951164569993065.jpg" alt>
            </div>
            <div class="song_text">[VIP专享]一周新歌推荐</div>
          </a>
          <a href>
            <div class="song_img">
              <img src="./imgs/109951164569993065.jpg" alt>
            </div>
            <div class="song_text">[VIP专享]一周新歌推荐</div>
          </a>
        </div>
      </div>
    </div>
    <!--新碟/新歌-->
    <div class="newDVD_tab_newsong">
      <div class="newDVD_tab_newsong_wrapper" >
		<liuyuno-tabs :tabData="tabs" :defaultIndex="tabindex" @tabClick='tabClick' />
		<scroll-view scroll-x class='scrollx_section_content'>
			<div v-if="!tabindex">
				<block >
				  <div class="scrollx_section_content_item">
				    <div class="scrollx_section_item_wrapper">
				      <div class="view_wrapper_image">
				        <img />
				      </div>
				      <div class="view_wrapper_intro">
				        <div class="wrapper_intro_title">
				          <span>全部</span>
				          <span>全部</span>
				        </div>
				        <div class="wrapper_intro_content left">
				          <span>标题</span>
				          <span>副标题</span>
				        </div>
				        <div class="wrapper_intro_content right">
				          <span>图</span>
				          <span>反对</span>
				        </div>
				        <div class="wrapper_intro_price">
				          <a>￥33 / <text>kg</text> <text >+</text> </a>
				        </div>
				      </div>
				    </div>
				  </div>
				</block>
				<block >
				  <div class="scrollx_section_content_item">
				    <div class="scrollx_section_item_wrapper">
				      <div class="view_wrapper_image">
				        <img />
				      </div>
				      <div class="view_wrapper_intro">
				        <div class="wrapper_intro_title">
				          <span>商品</span>
				          <span>描述</span>
				        </div>
				        <div class="wrapper_intro_content left">
				          <span>标题</span>
				          <span>副标题</span>
				        </div>
				        <div class="wrapper_intro_content right">
				          <span>图</span>
				          <span>反对</span>
				        </div>
				        <div class="wrapper_intro_price">
				          <a>￥33 / <text>kg</text> <text >+</text> </a>
				        </div>
				      </div>
				    </div>
				  </div>
				</block>
				<block >
				  <div class="scrollx_section_content_item">
				    <div class="scrollx_section_item_wrapper">
				      <div class="view_wrapper_image">
				        <img />
				      </div>
				      <div class="view_wrapper_intro">
				        <div class="wrapper_intro_title">
				          <span>商品</span>
				          <span>描述</span>
				        </div>
				        <div class="wrapper_intro_content left">
				          <span>标题</span>
				          <span>副标题</span>
				        </div>
				        <div class="wrapper_intro_content right">
				          <span>图</span>
				          <span>反对</span>
				        </div>
				        <div class="wrapper_intro_price">
				          <a>￥33 / <text>kg</text> <text >+</text> </a>
				        </div>
				      </div>
				    </div>
				  </div>
				</block>
			</div>
			<div v-if="tabindex">
				<block>
				  <div class="scrollx_section_content_item">
				    <div class="scrollx_section_item_wrapper">
				      <div class="view_wrapper_image">
				        <img />
				      </div>
				      <div class="view_wrapper_intro">
				        <div class="wrapper_intro_title">
				          <span>测试</span>
				          <span>测试</span>
				        </div>
				        <div class="wrapper_intro_content left">
				          <span>标题</span>
				          <span>副标题</span>
				        </div>
				        <div class="wrapper_intro_content right">
				          <span>图</span>
				          <span>反对</span>
				        </div>
				        <div class="wrapper_intro_price">
				          <a>￥33 / <text>kg</text> <text >+</text> </a>
				        </div>
				      </div>
				    </div>
				  </div>
				</block>
				<block >
				  <div class="scrollx_section_content_item">
				    <div class="scrollx_section_item_wrapper">
				      <div class="view_wrapper_image">
				        <img />
				      </div>
				      <div class="view_wrapper_intro">
				        <div class="wrapper_intro_title">
				          <span>商品</span>
				          <span>描述</span>
				        </div>
				        <div class="wrapper_intro_content left">
				          <span>标题</span>
				          <span>副标题</span>
				        </div>
				        <div class="wrapper_intro_content right">
				          <span>图</span>
				          <span>反对</span>
				        </div>
				        <div class="wrapper_intro_price">
				          <a>￥33 / <text>kg</text> <text >+</text> </a>
				        </div>
				      </div>
				    </div>
				  </div>
				</block>
				<block >
				  <div class="scrollx_section_content_item">
				    <div class="scrollx_section_item_wrapper">
				      <div class="view_wrapper_image">
				        <img />
				      </div>
				      <div class="view_wrapper_intro">
				        <div class="wrapper_intro_title">
				          <span>商品</span>
				          <span>描述</span>
				        </div>
				        <div class="wrapper_intro_content left">
				          <span>标题</span>
				          <span>副标题</span>
				        </div>
				        <div class="wrapper_intro_content right">
				          <span>图</span>
				          <span>反对</span>
				        </div>
				        <div class="wrapper_intro_price">
				          <a>￥33 / <text>kg</text> <text >+</text> </a>
				        </div>
				      </div>
				    </div>
				  </div>
				</block>
			</div>
		  </scroll-view>
      </div>
    </div>
  </div>
</template>

<script>
import Search from "../../components/search"
import Carousel from "../../components/carousel"
 import liuyunoTabs from "../../components/liuyuno-tabs/liuyuno-tabs.vue"
export default {
 data(){
	 return {
	defaultIndex: 0,
	tabindex:0,
	tabs: [
		{
			state: 0,
			text: '全部',
		},
		{
			state: 1,
			text: '测试'
		},
		{
			state: 2,
			text: '测试宽度'
		},
		{
			state: 3,
			text: '测试宽度三号'
		},
		{
			state: 4,
			text: '测试宽度四号小星星'
		},
		{
			state: 5,
			text: '测试宽度五号'
		},
	]
	 }
 },
  components:{
    Search,
    Carousel,
	liuyunoTabs
  },
  methods:{
		tabClick(index) {
				this.tabindex=index*1;
		},
  },
  onLoad:function(){
  	console.log('加载发现页')
  }
}
</script>

<style lang="less">
.found_page{
	background: #f5f5f5;
	padding-top: 25px;
	/*麦克风识别、播放中状态*/
	.find_page_header {
	  display: flex;
	  flex-wrap: nowrap;
	  align-items: center;
	  padding:12px;
	 text-align: center;
	 height: 42px;

	 background: #fff;
	  /*歌曲识别*/
	  .maike {
	    width: 30px;
	    height: 30px;
	    position: relative;
		margin: 0 3px;
	    display: inline-block;
		font-size: 20px;
	    a {
	      display: block;
	      width: 100%;
	      height: 100%;
	      text-decoration: none;
	      background: url(./imgs/mai.png) no-repeat;
	      background-size: 100% 100%;
	    }
	  }
	  .playing_audio{
		 width: 28px;
		 height: 28px;
	    position: relative;
	    display: inline-block;
		font-size: 20px;
		margin: 0 3px;
		  a{
			  display: block;
			  width: 100%;
			  height: 100%;
			  background: url(./imgs/playing.png) no-repeat;
			  background-size: 100% 100%;
			  text-align: center;
		  }
	  }
	}
	
	/*频道选择*/
	.category_channel {
	  height: 80px;
	   background: #fff;
	  padding: 5px;
	  .category_channel_wrapper {
	    width: 100%;
	    display: flex;
	    flex-wrap: nowrap;
	    align-items: center;
	    margin-top: 7px;
	    div {
	      margin: 0 37rpx;
	      width: 82rpx;
	      height: 82rpx;
		  text-align: center;
		  display: flex;
		  flex-wrap: wrap;
		  justify-content: center;
		  &.no-margin-left{
			  margin-left: 10px;
		  }
		  &.no-margin-right{
			  margin-right: 10px;
		  }
	      a {
	        display: block;
	        height: 100%;
	        width: 100%;
	        text-decoration: none;
	        background: #f10215;
	        border-radius: 50%;
	        display: flex;
	        align-items: center;
	        justify-content: center;
	        img {
	          display: block;
	          width: 54rpx;
	          height: 45rpx;
	          text-align: center;
	        }
	      }
	      span {
	        display: block;
	        color: #666;
	        line-height: 49rpx;
	        font-size:25rpx;
	        text-align: center;
	        white-space: nowrap;
	      }
	    }
	  }
	}
	/*推荐歌单*/
	.good_song_list {
	  overflow: hidden;
	  padding: 8px;
	   background: #fff;
	  .good_song_list_wrapper {
	    width: 100%;
	    overflow: hidden;
	    .songlist_header {
	      height: 30px;
	      width: 100%;
	      padding: 10px;
	      display: flex;
	      flex-wrap: nowrap;
	      align-items: center;
		  margin: 8px 0;
	      h4 {
		font-size: 15px;
			letter-spacing: 1px;
	        vertical-align: middle;
	        white-space: nowrap;
	      }
	      .songlist-plaza {
	        display: flex;
	        align-items: center;
	        justify-content: center;
	        border-radius: 15px;
	        border: 1px solid #ccc;
	        background: transparent;
	        line-height: 27px;
	        height: 27px;
	        text-align: center;
	        margin-left: 385rpx;
	
	        width: 170rpx;
	        vertical-align: middle;
	        span {
	          font-size: 14px;
			  color:#000;
	          text-align: center;
	        }
	      }
	    }
	    .hot_song_con {
	      display: flex;
	      flex-wrap: wrap;
	      width: 100%;
	      margin: auto;
		  justify-content: center;
		
	      a {
	        display: block;
	        width: 29%;
	        margin:2px 5px;
	        &:last-child {
	          margin-right: 0;
	        }
	        .song_img {
	          width: 100%;
	          height: 115px;
	          img {
	            display: block;
	            width: 100%;
	            height: 100%;
	          }
	        }
	        .song_text {
	          margin: 7px 0;
	          font-size: 12px;
	          color: #666;
	        }
	      }
	    }
	  }
	}
	/*新碟/新歌*/
	.newDVD_tab_newsong {
	  overflow: hidden;
	  padding: 8px;
	  height: 350px;
	   background: #fff;
	  .newDVD_tab_newsong_wrapper {
	    width: 100%;
	    overflow: hidden;
		.scrollx_section_content {
		  width: 100%;
		  white-space: nowrap;
		}
		
		.scrollx_section_content_item {
		  width: 626rpx;
		  height: 304rpx;
		  /* outline: 1px solid red; */
		  display: inline-block;
		  margin-left: 20rpx;
		  overflow: hidden;
		}
		
		.scrollx_section_content_item.last {
		  margin-right: 20rpx;
		}
		
		.scrollx_section_content .scrollx_section_content_item .scrollx_section_content_item_wrapper {
		  width: 572rpx;
		  height: 222rpx;
		  /* outline: 1px solid purple; */
		  margin-left: 30rpx;
		  margin-top: 40rpx;
		  overflow: hidden;
		}
		
		.view_wrapper_image {
		  width: 210rpx;
		  height: 180rpx;
		  margin-top: 20rpx;
		}
		
		.view_wrapper_image image {
		  width: 210rpx;
		  height: 180rpx;
		}
		
		.view_wrapper_intro {
		  width: 336rpx;
		  height: 222rpx;
		  /* outline: 1px solid green; */
		  float: right;
		  margin-top: -200rpx;
		  overflow: hidden;
		}
		
		.wrapper__intro__title {
		  width: 318rpx;
		}
		
		.wrapper_intro_title span {
		  overflow: hidden;
		  span-overflow: ellipsis;
		  white-space: nowrap;
		}
		
		.wrapper_intro_content {
		  width: 166rpx;
		  height: 64rpx;
		}
		
		.scrollx_section_content_item span {
		  display: block;
		}
		
		.wrapper_intro_title span:nth-child(2n) {
		  font-size: 22rpx;
		  color: #a9a9a9;
		  font-weight: blod;
		}
		
		.wrapper_intro_title span:nth-child(2n+1) {
		  font-size: 28rpx;
		  font-weight: blod;
		  color: #393939;
		}
		
		.wrapper_intro_content span:nth-child(2n+1) {
		  font-size: 34rpx;
		  font-weight: 800;
		  color: #434343;
		}
		
		.wrapper_intro_content span:nth-child(2n) {
		  font-size: 22rpx;
		  color: #a5a5a5;
		}
		
		.wrapper_intro_price {
		  width: 100%;
		  display: block;
		  overflow: hidden;
		  margin-top: 80rpx;
		}
		
		.wrapper_intro_price a {
		  color: #ff7c2a;
		  font-size: 26rpx;
		  font-weight: 600;
		}
		
		.wrapper_intro_price text:nth-child(1) {
		  color: #a6a6a6;
		  font-size: 24rpx;
		}
		
		.wrapper_intro_price text:nth-child(2) {
		  color: #25a4ff;
		  font-size: 40rpx;
		  float: right;
		  font-weight: 800;
		  /* margin-top: 6rpx; */
		  margin-right: 30rpx;
		}
	}
}
}
</style>
