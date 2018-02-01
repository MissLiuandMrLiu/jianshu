<template>
    <div>
        <my-header></my-header>
        <div class="note">
            <!--文章区域-->
            <div class="post">
                <!--正文-->
                <div class="article">
                    <h1 class="title">月薪三千,就该去死吗?</h1>
                    <div class="author">
                        <nuxt-link to="/u/123" class="avatar">
                            <img src="../../assets/img/default-avatar.jpg" alt="">
                        </nuxt-link>
                        <div class="info">
                            <span class="name">测试用户</span>
                            <a class="btn-sm" href="javascript:void(0)" :class="followObj" @click="isFollow" @mouseover="noFollow" @mouseleave="beFollow">
                                <i class="fa" :class="iconObj" ref="icon"></i>
                                <span ref="followWord">关注</span>
                            </a>
                            <div class="meta">
                                <span>2018.01.23 16:.9</span>
                                <span>字数 2273</span>
                                <span>阅读 882</span>
                                <span>评论 7</span>
                                <span>喜欢 34</span>
                            </div>
                        </div>
                    </div>
                    <div class="show-content">
                        <p>可能是春节快要到了，游子回家的旋律吹响，一年一度的“比头疼大赛”又要拉开大幕。比什么？比工作，比资产，比儿女，比婚姻。都市人携带着远方不为所知的辛苦，在同学相聚时，多了些虚伪；在朋友重逢时，少了些真诚。
                        </p>
                        <p>家乡是个让人又爱又恨的地方。有时，常看见有人自嘲：在外大老板，回乡二胖子；在外大哥大，回镇三孙子；在外大名媛，回村小豆子；在外喜当爹，回家好多爹——亲爹不倒，干爹飘飘。
                        </p>
                        <p>上周末，一众平台大号撰稿了类似“过年回家让你最害怕的事”这样一个主题。与往年千篇一律的抱怨答案不同，今年出来的评论里更多年轻人是对自己能力桎梏、工资不高的恐慌。当年的小愤青们长大，逐渐意识到生活的困境，其实这是一种成长。但是“爱搞事”的公众号另辟蹊径，就像《演员的诞生》节目会鬼魅剪辑一样，平台大编辑整合评论后，推出来一篇“工资三千的男人值不值得嫁”这样一个帖子，成功点燃新一轮的社会讨论。
                        </p>
                        <p>没办法，中国女性地位早已不是“重男轻女”的时代，代表着女权主义的评论清一色地给出“不能嫁”的结论，并嘲讽地说：“老娘自己都能赚到这个数，还要你这老爷们何用？”此等答案有几千人点赞，于是“代表底层大众”的“月薪三千的男人”被拉出来各种声讨。
                        </p>
                    </div>
                    <div class="show-foot">
                        <nuxt-link to="/nb/123" class="notebook">
                            <i class="fa fa-book"></i>
                            <span>我的文集</span>
                        </nuxt-link>
                        <div class="copyright">
                            © 著作权归作者所有
                        </div>
                    </div>
                    <div class="follow-detail">
                        <div class="info">
                            <nuxt-link class="avatar" to="/">
                                <img src="../../assets/img/default-avatar.jpg" alt="">
                            </nuxt-link>
                            <a href="javascript:void(0)" class="btn btn-success" :class="followObj" @click="isFollow" @mouseover="noFollow" @mouseleave="beFollow">
                                <i :class="iconObj" class="fa" ref="icon2"></i>
                                <span ref="followWord2">关注</span>
                            </a>
                            <nuxt-link class="title" to="/u/123">
                                测试用户
                            </nuxt-link>
                            <i class="fa fa-mars"></i>
                            <p>
                                写了 46873 字, 被 26 人关注, 获得了 95 个喜欢
                            </p>
                        </div>
                        <div class="signature">
                            微信公众号：得及 为城市里的不安和孤寂发声
                        </div>
                    </div>
                    <div class="meta-bottom">
                        <div class="like">
                            <div class="btn like-group" ref="likes">
                                <div class="btn-like">
                                    <a href="javascript:void(0)" @click="groupLike">
                                        <i class="fa fa-heart"></i>
                                        <span>喜欢</span>
                                    </a>
                                </div>
                                <div class="modal-wrap">
                                    <a href="">{{numberLike}}</a>
                                </div>
                            </div>
                        </div>
                        <div class="share-group">
                            <a href="javascript:void(0)" id="weibo" title="分享到微博">
                                <i class="fa fa-weibo weibo"></i>
                                <b-tooltip  target = "weibo"  placement="top" >
                                    分享到微博
                                </b-tooltip >
                            </a>
                            <a href="javascript:void(0)" id="weixin" title="分享到微信">
                                <i class="fa fa-weixin weixin"></i>
                                <b-tooltip  target = "weixin"  placement="top">
                                    分享到微信
                                </b-tooltip >
                            </a>
                            <a href="javascript:void(0)" id="qq" title="分享到qq">
                                <i class="fa fa-qq qq"></i>
                                <b-tooltip  target = "qq"  placement="top" >
                                    分享到qq
                                </b-tooltip >
                            </a>
                            <a href="javascript:void(0)" class="more-share" @focus="isShare=true" @blur="isShare=false">
                                更多分享
                            </a>
                        </div>
                        <div v-show="isShare" class="share-top">
                            <ul>
                                <li>
                                    <i class="fa fa-star"></i>
                                    <a href="">分享到空间</a>
                                </li>
                                <li>
                                    <i class="fa fa-star"></i>
                                    <a href="">分享到Twitter</a>
                                </li>
                                <li>
                                    <i class="fa fa-star"></i>
                                    <a href="">分享到Facebook</a>
                                </li>
                                <li>
                                    <i class="fa fa-star"></i>
                                    <a href="">分享到Goole+</a>
                                </li>
                                <li>
                                    <i class="fa fa-star"></i>
                                    <a href="">分享到豆瓣</a>
                                </li>
                            </ul>
                            <div class="three">

                            </div>
                        </div>

                    </div>
                </div>
            </div>
            <!--悬浮的操作框-->
            <div class="side-bar"></div>
            <!--对应的推荐阅读-->
            <div class="note-bottom"></div>
        </div>
    </div>
</template>

<script>
    import myHeader from '../../components/myHeader'
    export default {
        name: "_id",
        data(){
            return {
                followObj:{
                    'follow':true,
                    'following':false
                },
                iconObj:{
                    'fa-plus-square-o':true,
                    'fa-check':false
                },
                likeGroup:{
                    'like-group':true,
                    'like-groups':false
                },
                orange:false,
                numberLike:35,
                isShare:false
            }
        },
        components:{
            myHeader
        },
        methods:{
           isFollow:function () {
               let word = this.$refs.followWord.innerHTML;
               //这里预留关注ajax的操作
               this.followObj.follow = !this.followObj.follow;
               this.followObj.following = !this.followObj.following;
               this.iconObj['fa-plus-square-o'] = !this.iconObj['fa-plus-square-o'];
               this.iconObj['fa-check'] = !this.iconObj['fa-check'];
               this.$refs.followWord.innerHTML = word == '关注' ? '已关注' : '关注';
               this.$refs.followWord2.innerHTML = word == '关注' ? '已关注' : '关注';

           },
            noFollow:function () {
                let word = this.$refs.followWord.innerHTML;
                if(word == '已关注'){
                    this.$refs.followWord.innerHTML = '取消关注'
                    this.$refs.icon.className = 'fa fa-close'
                    this.$refs.followWord2.innerHTML = '取消关注'
                    this.$refs.icon2.className = 'fa fa-close'
                }
            },
            beFollow:function () {
                let word = this.$refs.followWord.innerHTML;
                if(word == '取消关注'){
                    this.$refs.followWord.innerHTML = '已关注'
                    this.$refs.icon.className = 'fa fa-check'
                    this.$refs.followWord2.innerHTML = '已关注'
                    this.$refs.icon2.className = 'fa fa-check'
                }
            },
            groupLike:function () {
                if(this.orange==false){
                    this.$refs.likes.classList.add('active')
                    this.numberLike = this.numberLike + 1
                    this.orange = true
                }else{
                    this.$refs.likes.classList.remove('active')
                    this.numberLike = this.numberLike - 1
                    this.orange = false
                }
            },
        }
    }
</script>

<style scoped>

</style>