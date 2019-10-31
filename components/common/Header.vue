<template>
  <div id="header" class="head">
    <div class="head_box js_head_box">
      <div class="weui-desktop-head__inner">
        <!-- 论坛顶部导航 -->
        <div check-reduce class="weui-desktop-head__inner_hd">
          <div class="weui-desktop-layout">
            <div class="weui-desktop-layout__side">
              <h1 class="weui-desktop-logo">
                <a href="/" :title="title" class="logo_mp_">🚀数据科学交流社区</a>
              </h1>
            </div>
          </div>
          <div class="block_nav selected">
            <a :href="community.link" class="block_nav_link">{{community.title}}</a>
          </div>
          <div class="block_nav" v-for="(page, index) in pages" :key="index">
            <a :href="page.link" class="block_nav_link">{{page.title}}</a>
          </div>
        </div>
        <!-- 移动端 -->
        <div class="header_ctrls js_header_ctrls">
          <div class="header_ctrls_extend">
            <div class="header_ctrls_meta header_ctrls_meta_navigation">
              <dl class="header_navigation_box">
                <dt class="header_navigation_box_header wxapp">小程序</dt>
                <dd class="header_navigation_box_body" style="display:none;">
                  <ul class="header_navigation_box_item_box">
                    <li class="header_navigation_box_item header_navigation_box_item_orientation">
                      <dl class="header_navigation_box_item_list">
                        <dt class="header_navigation_box_item_list_title">交流专区</dt>
                        <dd class="header_navigation_box_item_list_item">
                          <a
                            href="/community"
                            class="header_navigation_box_item_list_item_inner header_navigation_box_item_list_item_wxapp"
                          >
                            <span class="header_navigation_box_item_list_item_icon"></span>
                            <p class="header_navigation_box_item_list_item_desc">小程序</p>
                          </a>
                          <a
                            href="/community/minigame"
                            class="header_navigation_box_item_list_item_inner header_navigation_box_item_list_item_minigame"
                          >
                            <span class="header_navigation_box_item_list_item_icon"></span>
                            <p class="header_navigation_box_item_list_item_desc">小游戏</p>
                          </a>
                          <a
                            href="/community/enterprisewechat"
                            class="header_navigation_box_item_list_item_inner header_navigation_box_item_list_item_wxenterprise"
                          >
                            <span class="header_navigation_box_item_list_item_icon"></span>
                            <p class="header_navigation_box_item_list_item_desc">企业微信</p>
                          </a>
                          <a
                            href="/community/pay"
                            class="header_navigation_box_item_list_item_inner header_navigation_box_item_list_item_wxpay"
                          >
                            <span
                              class="header_navigation_box_item_list_item_icon header_navigation_box_item_list_item_pay"
                            ></span>
                            <p class="header_navigation_box_item_list_item_desc">微信支付</p>
                          </a>
                        </dd>
                      </dl>
                    </li>
                    <li check-reduce class="header_navigation_box_item">
                      <a
                        href="/community/servicemarket"
                        target="_blank"
                        class="header_navigation_box_item_inner"
                      >
                        <dl class="header_navigation_box_item_list">
                          <dt class="header_navigation_box_item_list_title">服务平台</dt>
                        </dl>
                      </a>
                      <a
                        href="/community/business"
                        target="_blank"
                        class="header_navigation_box_item_inner"
                      >
                        <dl class="header_navigation_box_item_list">
                          <dt class="header_navigation_box_item_list_title">微信学院</dt>
                        </dl>
                      </a>
                      <a
                        itemprop="url"
                        target="_blank"
                        href="https://developers.weixin.qq.com/miniprogram/dev/framework/"
                        class="header_navigation_box_item_inner"
                      >
                        <dl class="header_navigation_box_item_list">
                          <dt class="header_navigation_box_item_list_title">文档</dt>
                        </dl>
                      </a>
                    </li>
                    <li class="header_navigation_box_item">
                      <a
                        href="/community/personal/oCJUsw3GtB9rYcqSscQ9hgRBly3c"
                        target="_blank"
                        class="header_navigation_box_item_inner"
                      >
                        <dl class="header_navigation_box_item_list">
                          <dt class="header_navigation_box_item_list_title">我的账号</dt>
                        </dl>
                      </a>
                      <a
                        href="/community/notify"
                        target="_blank"
                        class="header_navigation_box_item_inner"
                      >
                        <dl class="header_navigation_box_item_list">
                          <dt class="header_navigation_box_item_list_title">消息</dt>
                        </dl>
                      </a>
                    </li>
                  </ul>
                </dd>
              </dl>
            </div>
            <div check-reduce class="js_search_header_box header_ctrls_meta top_search_box for_pc">
              <a href="javascript:;" class="js_search_btn search_switch">
                <i class="icon_search"></i>
              </a>
              <span class="js_input_box search_input_box active">
                <input type="text" placeholder="搜索你要的内容" value class="js_input" />
                <!---->
              </span>
              <!---->
            </div>
            <div
              id="user-bar"
              data-openid="oCJUsw3GtB9rYcqSscQ9hgRBly3c"
              data-nickname="Alchemist"
              check-reduce
              class="dib"
            >
              <div class="header_ctrls_meta top_notice_box header_adjust_height">
                <a href="javascript:;" class="account_inbox_switch js_notice_box_switch">
                  <i class="icon_inbox"></i>
                  <!---->
                </a>
                <div
                  class="account_message_box skin_pop js_account_notice_box"
                  style="display:none;"
                >
                  <div class="skin_pop_inner account_message_box_inner">
                    <div class="account_message_box_hd global_mod">
                      <div class="global_info global_info_item global_info_notice active">系统消息</div>
                      <div class="global_info global_info_item global_info_private">
                        私信
                        <span class="unread-tag-small" style="display:none;"></span>
                      </div>
                    </div>
                    <div class="account_message_box_bd">
                      <ul class="account_message_list js_message_list" style="display:;">
                        <li class="account_message_list_empty">暂无消息</li>
                      </ul>
                      <ul class="account_private_list" style="display:none;">
                        <li class="account_message_list_empty">暂无私信</li>
                      </ul>
                    </div>
                    <div class="skin_pop_ft account_message_box_ft">
                      <a href="javascript:;">查看全部</a>
                    </div>
                  </div>
                  <i class="icon_skin_pop_arrow account_message_arrow"></i>
                </div>
              </div>
              <div class="header_ctrls_meta top_user_box">
                <a href="/community/personal/oCJUsw3GtB9rYcqSscQ9hgRBly3c" class="top_user_switch">
                  <img
                    src="https://wx.qlogo.cn/mmhead/ofvnGicEPbfSYnW2cHPOxFOh84icteRdbN0ILBjTkw6BeuOlBJPLNDlQ/0"
                    alt
                    class="user_avatar"
                  />
                </a>
                <div class="skin_pop">
                  <div class="skin_pop_inner">
                    <div class="skin_pop_bd">
                      <a
                        href="/community/personal/oCJUsw3GtB9rYcqSscQ9hgRBly3c"
                        title="Alchemist"
                        class="user_name"
                      >Alchemist</a>
                    </div>
                    <!---->
                    <div class="skin_pop_ft skin_pop_ft_logout">
                      <a id="logout" class="javascript:;">退出</a>
                    </div>
                  </div>
                  <i class="icon_skin_pop_arrow"></i>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div check-reduce class="block_nav_wrp" v-if="isShowTopic">
      <div class="block_nav_wrp_cont">
        <ul class="block_navs">
          <li class="block_nav" :class="{'selected': index === 0}" v-for="(item, index) in topic" :key="index">
            <a :href="item.link" class="block_nav_link" :class="{'router-link-active': index === 0}">{{item.cnName}}</a>
          </li>
        </ul>
        <div class="search_hold"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: 'test'
    },
    isShowTopic: {
      type: Boolean,
      default: true
    }
  },
  
  data() {
    return {
      community: {
        title: '交流社区'
      },
      pages: [
        {
          title: '文档中心',
          self: false,
          link: '/docs'
        },
        {
          title: '演练场',
          self: false,
          link: '/playground'
        }
      ],
      topic: [
        {
          enName: 'numpy',
          cnName: 'numpy',
          id: 'numpy',
          self: true,
          link: '/numpy'
        },
        {
          enName: 'pandas',
          cnName: 'pandas',
          id: 'pandas',
          self: true,
          link: '/pandas'
        },
        {
          enName: 'matplotlib',
          cnName: 'matplotlib',
          id: 'matplotlib',
          self: true,
          link: '/matplotlib'
        },
        {
          enName: 'seaborn',
          cnName: 'seaborn',
          id: 'seaborn',
          self: true,
          link: '/seaborn'
        },
        {
          enName: 'TensorFlow',
          cnName: 'TensorFlow',
          id: 'tensorflow',
          self: true,
          link: '/tensorflow'
        }
      ]
    }
  }
};
</script>
