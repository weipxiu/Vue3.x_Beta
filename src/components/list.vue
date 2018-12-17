<template>
  <div class="continar-left">
    <div
      class="text"
      v-if="listData && listData.length>0"
      v-for="(item, index) in listData"
      :key="index"
    >
      <div class="img-left">
        <a
          class="read-more"
          href="https://www.weipxiu.com/2433.html"
          target="_blank"
        >
          <img
            width="220"
            height="150"
            src="https://www.weipxiu.com/wp-content/uploads/2018/07/xiaovue.png"
            class="attachment-post-thumbnail size-post-thumbnail wp-post-image"
            alt=""
          > </a>
      </div>
      <div class="text_right">
        <h2>
          <span>
            <ul class="post-categories">
              <li><a
                  href="https://www.weipxiu.com/category/frontend/js-frame"
                  rel="category tag"
                >Js前端框架</a></li>
            </ul><i></i>
          </span>
          <a
            :href="item.link"
            target="_blank"
            :title="item.title.rendered"
          >
            {{item.title.rendered}}</a>
        </h2>
        <div class="entry-meta">
          <a href="https://www.weipxiu.com">唯品秀</a>
          <i class="space">•</i>
          <a href="#">
            <!-- <? /*php the_field('original'); */?> -->
            原创 </a>
          <i class="space">•</i>
          管理员 <a
            href="#"
            class="comments-number"
          >
            <span></span>
          </a>
        </div>
        <h3>
          在开发脚手架项目中，我们经常需要去根据环境打包代码，主要是改变对应的接口，上测试要打包对应的测试接口地址，上正式应该打包时候用正式，这需要我们就有...
          <!--文章内容-->
        </h3>
        <a
          class="read-more"
          href="https://www.weipxiu.com/2433.html"
          target="_blank"
        >阅读全文<i class="fa fa-chevron-circle-right"></i></a>
        <p class="l">
          <!-- <span>
							<a href=" ">
								<i class="fa fa-calendar">&nbsp;</i>							</a>
						</span> -->
          <span><i
              class="fa fa-calendar"
              aria-hidden="true"
            ></i>&nbsp;
            2018年12月12日</span>
          <span>
            <a href="https://www.weipxiu.com/2433.html ">
              <i class="iconfont icon-liulan"></i>&nbsp;
              42℃
            </a>
          </span>
          <span class="comm">
            <a href="https://www.weipxiu.com/2433.html ">
              <i class="iconfont icon-pinglun2"></i>
              0 条评论
            </a>
          </span>
          <span class="post-like">
            <a
              href="javascript:;"
              data-action="ding"
              data-id="2433"
              class="favorite"
            >
              <i class="fa fa-thumbs-o-up"></i>
              <span class="count">
                2 </span>喜欢
            </a>
          </span>
          <span class="r"></span>
        </p>
        <em><a href="">顶</a></em> <!-- <span class="new-icon">NEW</span> -->
      </div>
      <!-- <font class="s_bar"></font> -->
      <!--竖条-->
    </div>
  </div>

</template>

<script>
import API from '@/api'
export default {
  name: 'sidebar',
  data() {
    return {
      listData: []
    }
  },
  created() {
    API.getArticleList().then((res) => {
      console.log(res)
      this.listData = res.data
    }).catch(function (err) {
      console.log(err);
    })
  }
}
</script>

<style scoped>
</style>
