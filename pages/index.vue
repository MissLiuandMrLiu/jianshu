<template>
    <div>
        <my-header></my-header>
        <div class="index my-container">
            <div class="row">
                <div class="col-8 main">
                    <!--banner-->
                    <div class="banner">
                        <div v-swiper:mySwiper="swiperOption">
                            <div class="swiper-wrapper">
                                <div class="swiper-slide" v-for="banner in banners">
                                    <img :src="banner">
                                </div>
                            </div>
                            <div class="swiper-pagination swiper-pagination-white"></div>
                            <div class="swiper-button-prev swiper-button-white" slot="button-prev"></div>
                            <div class="swiper-button-next swiper-button-white" slot="button-next"></div>
                        </div>
                    </div>
                    <!--推荐专题-->
                    <div class="recommend-collection">
                        <nuxt-link to="/collection/123">
                            <img src="../assets/img/collection1.jpg" alt="">
                            <span>读书</span>
                        </nuxt-link>
                        <nuxt-link to="/collection/123">
                            <img src="../assets/img/collection2.jpg" alt="">
                            <span>人文社科</span>
                        </nuxt-link>
                        <nuxt-link to="/collection/123">
                            <img src="../assets/img/collection3.jpg" alt="">
                            <span>故事</span>
                        </nuxt-link>
                        <nuxt-link to="/collection/123">
                            <img src="../assets/img/collection1.jpg" alt="">
                            <span>读书</span>
                        </nuxt-link>
                        <nuxt-link to="/collection/123">
                            <img src="../assets/img/collection2.jpg" alt="">
                            <span>人文社科</span>
                        </nuxt-link>
                        <nuxt-link to="/collection/123">
                            <img src="../assets/img/collection3.jpg" alt="">
                            <span>故事</span>
                        </nuxt-link>
                        <nuxt-link class="more-hot-collection" to="/collection/123">
                            更多热门专题
                            <i class="fa fa-angle-right"></i>
                        </nuxt-link>
                    </div>
                    <div class="split-line"></div>
                    <!--文章列表-->
                    <div id="list-container">
                        <ul class="note-list">
                            <li class="have-img">
                            <nuxt-link class="wrap-img" to="/p/123">
                                <img src="../assets/img/pic.jpg" alt="">
                            </nuxt-link>
                            <div class="content">
                                <div class="author">
                                    <nuxt-link to="/u/123" class="avatar">
                                        <img src="../assets/img/default-avatar.jpg" alt="">
                                    </nuxt-link>
                                    <div class="info">
                                        <nuxt-link to="/u/123" class="nickname">测试用户
                                        </nuxt-link>
                                        <span class="time">8小时前</span>
                                    </div>
                                </div>
                                <nuxt-link class="title" to="/p/123">
                                    如何把书中的知识转化成能力?这是我见过的最好的回答
                                </nuxt-link>
                                <p class="abstract">
                                    随着知识经济的兴起，读书的重要性得到了大家的普遍认同，于是市场上出现很多读书方法，比如速度、多读、慢读、列读……不管你采用哪一种读书方法，最终都要回归到“行动”二字上，正如陆...
                                </p>
                                <div class="meta">
                                    <nuxt-link to="/collection/123" class="collection-tag">
                                        短片小说
                                    </nuxt-link>
                                    <nuxt-link class="tag" to="/p/123">
                                        <i class="fa fa-eye"></i>
                                        579
                                    </nuxt-link>
                                    <nuxt-link class="tag" to="/p/123">
                                        <i class="fa fa-comment"></i>
                                        200
                                    </nuxt-link>
                                    <span>
                                            <i class="fa fa-heart"></i>
                                            546
                                        </span>
                                </div>
                            </div>
                        </li>
                            <li class="have-img">
                                <div class="content">
                                    <div class="author">
                                        <nuxt-link to="/u/123" class="avatar">
                                            <img src="../assets/img/default-avatar.jpg" alt="">
                                        </nuxt-link>
                                        <div class="info">
                                            <nuxt-link to="/u/123" class="nickname">测试用户
                                            </nuxt-link>
                                            <span class="time">8小时前</span>
                                        </div>
                                    </div>
                                    <nuxt-link class="title" to="/p/123">
                                        如何把书中的知识转化成能力?这是我见过的最好的回答
                                    </nuxt-link>
                                    <p class="abstract">
                                        随着知识经济的兴起，读书的重要性得到了大家的普遍认同，于是市场上出现很多读书方法，比如速度、多读、慢读、列读……不管你采用哪一种读书方法，最终都要回归到“行动”二字上，正如陆...
                                    </p>
                                    <div class="meta">
                                        <nuxt-link to="/collection/123" class="collection-tag">
                                            短片小说
                                        </nuxt-link>
                                        <nuxt-link class="tag" to="/p/123">
                                            <i class="fa fa-eye"></i>
                                            579
                                        </nuxt-link>
                                        <nuxt-link class="tag" to="/p/123">
                                            <i class="fa fa-comment"></i>
                                            200
                                        </nuxt-link>
                                        <span>
                                            <i class="fa fa-heart"></i>
                                            546
                                        </span>
                                    </div>
                                </div>
                            </li>
                            <li class="have-img">
                                <nuxt-link class="wrap-img" to="/p/123">
                                    <img src="../assets/img/pic.jpg" alt="">
                                </nuxt-link>
                                <div class="content">
                                    <div class="author">
                                        <nuxt-link to="/u/123" class="avatar">
                                            <img src="../assets/img/default-avatar.jpg" alt="">
                                        </nuxt-link>
                                        <div class="info">
                                            <nuxt-link to="/u/123" class="nickname">测试用户
                                            </nuxt-link>
                                            <span class="time">8小时前</span>
                                        </div>
                                    </div>
                                    <nuxt-link class="title" to="/p/123">
                                        如何把书中的知识转化成能力?这是我见过的最好的回答
                                    </nuxt-link>
                                    <p class="abstract">
                                        随着知识经济的兴起，读书的重要性得到了大家的普遍认同，于是市场上出现很多读书方法，比如速度、多读、慢读、列读……不管你采用哪一种读书方法，最终都要回归到“行动”二字上，正如陆...
                                    </p>
                                    <div class="meta">
                                        <nuxt-link to="/collection/123" class="collection-tag">
                                            短片小说
                                        </nuxt-link>
                                        <nuxt-link class="tag" to="/p/123">
                                            <i class="fa fa-eye"></i>
                                            579
                                        </nuxt-link>
                                        <nuxt-link class="tag" to="/p/123">
                                            <i class="fa fa-comment"></i>
                                            200
                                        </nuxt-link>
                                        <span>
                                            <i class="fa fa-heart"></i>
                                            546
                                        </span>
                                    </div>
                                </div>
                            </li>
                            <li class="have-img">

                                <div class="content">
                                    <div class="author">
                                        <nuxt-link to="/u/123" class="avatar">
                                            <img src="../assets/img/default-avatar.jpg" alt="">
                                        </nuxt-link>
                                        <div class="info">
                                            <nuxt-link to="/u/123" class="nickname">测试用户
                                            </nuxt-link>
                                            <span class="time">8小时前</span>
                                        </div>
                                    </div>
                                    <nuxt-link class="title" to="/p/123">
                                        如何把书中的知识转化成能力?这是我见过的最好的回答
                                    </nuxt-link>
                                    <p class="abstract">
                                        随着知识经济的兴起，读书的重要性得到了大家的普遍认同，于是市场上出现很多读书方法，比如速度、多读、慢读、列读……不管你采用哪一种读书方法，最终都要回归到“行动”二字上，正如陆...
                                    </p>
                                    <div class="meta">
                                        <nuxt-link to="/collection/123" class="collection-tag">
                                            我喜欢你
                                        </nuxt-link>
                                        <nuxt-link class="tag" to="/p/123">
                                            <i class="fa fa-eye"></i>
                                            579
                                        </nuxt-link>
                                        <nuxt-link class="tag" to="/p/123">
                                            <i class="fa fa-comment"></i>
                                            200
                                        </nuxt-link>
                                        <span>
                                            <i class="fa fa-heart"></i>
                                            546
                                        </span>
                                    </div>
                                </div>
                            </li>
                            <li class="have-img">
                                <nuxt-link class="wrap-img" to="/p/123">
                                    <img src="../assets/img/pic.jpg" alt="">
                                </nuxt-link>
                                <div class="content">
                                    <div class="author">
                                        <nuxt-link to="/u/123" class="avatar">
                                            <img src="../assets/img/default-avatar.jpg" alt="">
                                        </nuxt-link>
                                        <div class="info">
                                            <nuxt-link to="/u/123" class="nickname">测试用户
                                            </nuxt-link>
                                            <span class="time">8小时前</span>
                                        </div>
                                    </div>
                                    <nuxt-link class="title" to="/p/123">
                                        如何把书中的知识转化成能力?这是我见过的最好的回答
                                    </nuxt-link>
                                    <p class="abstract">
                                        随着知识经济的兴起，读书的重要性得到了大家的普遍认同，于是市场上出现很多读书方法，比如速度、多读、慢读、列读……不管你采用哪一种读书方法，最终都要回归到“行动”二字上，正如陆...
                                    </p>
                                    <div class="meta">
                                        <nuxt-link to="/collection/123" class="collection-tag">
                                            短片小说
                                        </nuxt-link>
                                        <nuxt-link class="tag" to="/p/123">
                                            <i class="fa fa-eye"></i>
                                            579
                                        </nuxt-link>
                                        <nuxt-link class="tag" to="/p/123">
                                            <i class="fa fa-comment"></i>
                                            200
                                        </nuxt-link>
                                        <span>
                                            <i class="fa fa-heart"></i>
                                            546
                                        </span>
                                    </div>
                                </div>
                            </li>
                            <li class="have-img">
                                <nuxt-link class="wrap-img" to="/p/123">
                                    <img src="../assets/img/pic.jpg" alt="">
                                </nuxt-link>
                                <div class="content">
                                    <div class="author">
                                        <nuxt-link to="/u/123" class="avatar">
                                            <img src="../assets/img/default-avatar.jpg" alt="">
                                        </nuxt-link>
                                        <div class="info">
                                            <nuxt-link to="/u/123" class="nickname">测试用户
                                            </nuxt-link>
                                            <span class="time">8小时前</span>
                                        </div>
                                    </div>
                                    <nuxt-link class="title" to="/p/123">
                                        如何把书中的知识转化成能力?这是我见过的最好的回答
                                    </nuxt-link>
                                    <p class="abstract">
                                        随着知识经济的兴起，读书的重要性得到了大家的普遍认同，于是市场上出现很多读书方法，比如速度、多读、慢读、列读……不管你采用哪一种读书方法，最终都要回归到“行动”二字上，正如陆...
                                    </p>
                                    <div class="meta">
                                        <nuxt-link to="/collection/123" class="collection-tag">
                                            短片小说
                                        </nuxt-link>
                                        <nuxt-link class="tag" to="/p/123">
                                            <i class="fa fa-eye"></i>
                                            579
                                        </nuxt-link>
                                        <nuxt-link class="tag" to="/p/123">
                                            <i class="fa fa-comment"></i>
                                            200
                                        </nuxt-link>
                                        <span>
                                            <i class="fa fa-heart"></i>
                                            546
                                        </span>
                                    </div>
                                </div>
                            </li>
                            <li class="have-img">
                                <nuxt-link class="wrap-img" to="/p/123">
                                    <img src="../assets/img/pic.jpg" alt="">
                                </nuxt-link>
                                <div class="content">
                                    <div class="author">
                                        <nuxt-link to="/u/123" class="avatar">
                                            <img src="../assets/img/default-avatar.jpg" alt="">
                                        </nuxt-link>
                                        <div class="info">
                                            <nuxt-link to="/u/123" class="nickname">测试用户
                                            </nuxt-link>
                                            <span class="time">8小时前</span>
                                        </div>
                                    </div>
                                    <nuxt-link class="title" to="/p/123">
                                        如何把书中的知识转化成能力?这是我见过的最好的回答
                                    </nuxt-link>
                                    <p class="abstract">
                                        随着知识经济的兴起，读书的重要性得到了大家的普遍认同，于是市场上出现很多读书方法，比如速度、多读、慢读、列读……不管你采用哪一种读书方法，最终都要回归到“行动”二字上，正如陆...
                                    </p>
                                    <div class="meta">
                                        <nuxt-link to="/collection/123" class="collection-tag">
                                            短片小说
                                        </nuxt-link>
                                        <nuxt-link class="tag" to="/p/123">
                                            <i class="fa fa-eye"></i>
                                            579
                                        </nuxt-link>
                                        <nuxt-link class="tag" to="/p/123">
                                            <i class="fa fa-comment"></i>
                                            200
                                        </nuxt-link>
                                        <span>
                                            <i class="fa fa-heart"></i>
                                            546
                                        </span>
                                    </div>
                                </div>
                            </li>
                            <li class="have-img">
                                <nuxt-link class="wrap-img" to="/p/123">
                                    <img src="../assets/img/pic.jpg" alt="">
                                </nuxt-link>
                                <div class="content">
                                    <div class="author">
                                        <nuxt-link to="/u/123" class="avatar">
                                            <img src="../assets/img/default-avatar.jpg" alt="">
                                        </nuxt-link>
                                        <div class="info">
                                            <nuxt-link to="/u/123" class="nickname">测试用户
                                            </nuxt-link>
                                            <span class="time">8小时前</span>
                                        </div>
                                    </div>
                                    <nuxt-link class="title" to="/p/123">
                                        如何把书中的知识转化成能力?这是我见过的最好的回答
                                    </nuxt-link>
                                    <p class="abstract">
                                        随着知识经济的兴起，读书的重要性得到了大家的普遍认同，于是市场上出现很多读书方法，比如速度、多读、慢读、列读……不管你采用哪一种读书方法，最终都要回归到“行动”二字上，正如陆...
                                    </p>
                                    <div class="meta">
                                        <nuxt-link to="/collection/123" class="collection-tag">
                                            短片小说
                                        </nuxt-link>
                                        <nuxt-link class="tag" to="/p/123">
                                            <i class="fa fa-eye"></i>
                                            579
                                        </nuxt-link>
                                        <nuxt-link class="tag" to="/p/123">
                                            <i class="fa fa-comment"></i>
                                            200
                                        </nuxt-link>
                                        <span>
                                            <i class="fa fa-heart"></i>
                                            546
                                        </span>
                                    </div>
                                </div>
                            </li>
                        </ul>
                    </div>
                    <!--阅读更多-->
                    <nuxt-link to="/" class="load-more">
                        阅读更多
                    </nuxt-link>
                </div>
                <div class="col-4 aside">
                    <div class="board">
                        <nuxt-link to="/">
                            <img src="../assets/img/banne1.png">
                        </nuxt-link>
                        <nuxt-link to="/">
                            <img src="../assets/img/banner2.png">
                        </nuxt-link>
                        <nuxt-link to="/">
                            <img src="../assets/img/banner3.png">
                        </nuxt-link>
                        <nuxt-link to="/">
                            <img src="../assets/img/banner4.png">
                        </nuxt-link>
                        <nuxt-link to="/">
                            <img src="../assets/img/banner5.png">
                        </nuxt-link>
                    </div>
                    <nuxt-link class="download" to="/">
                        <!--二维码-->
                        <img src="../assets/img/二维码.jpg" alt="">
                    </nuxt-link>
                    <div class="recommend-author">
                        <div class="title">
                            <span>推荐作者</span>
                            <a href="javascript:void(0)" class="page-change" @click="rotate">
                                <i ref="refresh" class="fa fa-refresh"></i>
                                换一批
                            </a>
                        </div>
                        <ul class="list">
                            <li>
                                <nuxt-link class="avatar" to="/u/123">
                                    <img src="../assets/img/default-avatar.jpg" alt="">
                                </nuxt-link>
                                <nuxt-link class="follow" to="/u/123">
                                    <i class="fa fa-plus-square-o"></i>
                                    关注
                                </nuxt-link>
                                <nuxt-link class="name" to="/u/123">
                                    李博文
                                </nuxt-link>
                                <p>
                                    写了152.9K·7.2K喜欢
                                </p>
                            </li>
                            <li>
                                <nuxt-link class="avatar" to="/u/123">
                                    <img src="../assets/img/default-avatar.jpg" alt="">
                                </nuxt-link>
                                <nuxt-link class="follow" to="/u/123">
                                    <i class="fa fa-plus-square-o"></i>
                                    关注
                                </nuxt-link>
                                <nuxt-link class="name" to="/u/123">
                                    李博文
                                </nuxt-link>
                                <p>
                                    写了152.9K·7.2K喜欢
                                </p>
                            </li>
                            <li>
                                <nuxt-link class="avatar" to="/u/123">
                                    <img src="../assets/img/default-avatar.jpg" alt="">
                                </nuxt-link>
                                <nuxt-link class="follow" to="/u/123">
                                    <i class="fa fa-plus-square-o"></i>
                                    关注
                                </nuxt-link>
                                <nuxt-link class="name" to="/u/123">
                                    李博文
                                </nuxt-link>
                                <p>
                                    写了152.9K·7.2K喜欢
                                </p>
                            </li>
                            <li>
                                <nuxt-link class="avatar" to="/u/123">
                                    <img src="../assets/img/default-avatar.jpg" alt="">
                                </nuxt-link>
                                <nuxt-link class="follow" to="/u/123">
                                    <i class="fa fa-plus-square-o"></i>
                                    关注
                                </nuxt-link>
                                <nuxt-link class="name" to="/u/123">
                                    李博文
                                </nuxt-link>
                                <p>
                                    写了152.9K·7.2K喜欢
                                </p>
                            </li>
                            <li>
                                <nuxt-link class="avatar" to="/u/123">
                                    <img src="../assets/img/default-avatar.jpg" alt="">
                                </nuxt-link>
                                <nuxt-link class="follow" to="/u/123">
                                    <i class="fa fa-plus-square-o"></i>
                                    关注
                                </nuxt-link>
                                <nuxt-link class="name" to="/u/123">
                                    李博文
                                </nuxt-link>
                                <p>
                                    写了152.9K·7.2K喜欢
                                </p>
                            </li>
                        </ul>
                        <nuxt-link class="find-more" to="/">
                            查看更多
                            <i class="fa fa-angle-right"></i>
                        </nuxt-link>
                    </div>
                </div>
            </div>
        </div>
        <footer class="my-container footer">
            <div class="row">
                <div class="col-12">
                    <div class="footer-row">
                        <nuxt-link to="/">
                            关于简书
                        </nuxt-link>
                        <em>·</em>
                        <nuxt-link to="/">
                            联系我们
                        </nuxt-link>
                        <em>·</em>
                        <nuxt-link to="/">
                            加入我们
                        </nuxt-link>
                        <em>·</em>
                        <nuxt-link to="/">
                            简书出版
                        </nuxt-link>
                        <em>·</em>
                        <nuxt-link to="/">
                            品牌与徽标
                        </nuxt-link>
                        <em>·</em>
                        <nuxt-link to="/">
                            帮助中心
                        </nuxt-link>
                        <em>·</em>
                        <nuxt-link to="/">
                            合作伙伴
                        </nuxt-link>
                    </div>
                </div>
            </div>
        </footer>
    </div>
</template>
<script>
    import myHeader from '../components/myHeader'
    export default {
        data(){
            return {
                banners:[
                    '/lunbo1.jpg',
                    '/lunbo2.jpg',
                    '/lunbo3.jpg',
                    '/lunbo4.jpg'
                ],
                swiperOption: {
                        /*loop: true,
                        slidesPerView: 'auto',
                        centeredSlides: true,
                        spaceBetween: 30,*/
                    autoplay:{
                        delay:3000,//切换时间
                        stopOnLastSlide:false,//是否停止在最后一张
                        disableOnInteraction:false,//禁止轮播
                    },
                    pagination: {
                        el: '.swiper-pagination',
                        dynamicBullets: true
                    },
                    navigation: {
                        nextEl: '.swiper-button-next',
                        prevEl: '.swiper-button-prev'
                    }
                },
                deg:360
            }
        },
        components:{
            myHeader
        },
        methods:{
            rotate:function () {
                this.deg = this.deg + 360;
                this.$refs.refresh.style.transform = `rotate(${this.deg}deg)`;
            }
        }
    }
</script>
<style scoped>
    .swiper-button-next {

    }
    .swiper-button-prev {

    }

</style>