<template>
    <div>
        <div class="top-article">
            <div class="top-article__content center">
                <h1 class="top-article__heading">Articles & News</h1>

                <BreadcrmbsComp :breadcrumbs="breadcrumbs" slot=""/>
                 <ul class="top-article__breadcrumbs">
                    <li class="top-article__li">Home</li>
                    <li class="top-article__li">Blog</li>
                </ul> 

            </div>
        </div>
        <main class="article-content center ">
            <article class="post">
                <h2 class="post__heading">Latest Post</h2>
                <section class="post__block">
                    <img :src="postImg" alt="post pic" class="post__img">
                    <div class="post__content">
                        <h4 class="post__content_title">
                            Low Cost Latest Invented Interior Designing Ideas
                        </h4>
                        <p class="post__content_text">
                            Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpis dignissim maximus.posuere in.Contrary to popular belief. 
                        </p>
                        <p class="post__content_text">
                            Lorem Ipsum is not simply random text. It has roots in a piece of classic
                        </p>
                        <div class="post__content_footer">
                            <p class="post__content_date">26 December,2022 </p>
                            <svg xmlns="http://www.w3.org/2000/svg" width="52" height="53" viewBox="0 0 52 53" fill="none">
                                <circle cx="26" cy="26.5" r="26" fill="#F4F0EC"/>
                                <path d="M23.771 33.1855L29.7139 26.4998L23.771 19.8141" stroke="#292F36" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                            </svg>
                        </div>
                    </div>
                </section>
            </article>
            <article class="news-blog">
                <div class="news__heading">
                    Articles & News
                </div>


                <NewsCardComp :products="products" />

                <div class="news__conteiner">
                    <ul class="pagination">
                        <li class="pagination__li number">
                            <svg xmlns="http://www.w3.org/2000/svg" width="53" height="52" viewBox="0 0 53 52" fill="none">
                                <circle cx="26.5" cy="26" r="26" fill="#F4F0EC"/>
                            </svg>
                        </li>
                        <li class="pagination__li number">
                            <svg xmlns="http://www.w3.org/2000/svg" width="53" height="52" viewBox="0 0 53 52" fill="none">
                                <circle cx="26.5" cy="26" r="25.5" stroke="#CDA274"/>
                            </svg>
                        </li>
                        <li class="pagination__li number">
                            <svg xmlns="http://www.w3.org/2000/svg" width="53" height="52" viewBox="0 0 53 52" fill="none">
                                <circle cx="26.5" cy="26" r="25.5" stroke="#CDA274"/>
                            </svg>
                        </li>
                        <li class="pagination__li">
                            <svg xmlns="http://www.w3.org/2000/svg" width="53" height="52" viewBox="0 0 53 52" fill="none">
                                <circle cx="26.5" cy="26" r="25.5" stroke="#CDA274"/>
                                <path d="M23.5571 32L29.5 25.3143L23.5571 18.6286" stroke="#292F36" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                            </svg>
                        </li>
                    </ul>
                </div>
            </article>
        </main>
    </div>
  </template>
  
  <script>
import news1 from '@/assets/new-img/news_1.png'
import news2 from '@/assets/new-img/news_2.png'
import news3 from '@/assets/new-img/news_3.png'
import news4 from '@/assets/new-img/news_4.png'
import news5 from '@/assets/new-img/news_5.png'
import news6 from '@/assets/new-img/news_6.png'
import postImg from '@/assets/post_img.png'

import BreadcrmbsComp from '@/components/BreadcrumbsComp.vue'
import NewsCardComp from '@/components/NewsCardComponent.vue'

  export default {
    name: 'BlogComp',
    components: {
        NewsCardComp,
        BreadcrmbsComp
    },
    props: {
     
    },
    data() {
        return {  
            breadcrumbs: ['Home', 'Blog'],   
            postImg,    
            products: [
                {
                    imgUrl: news1,
                    heading: 'Let’s Get Solution For Building Construction Work',
                    date: '26 December,2022',
                    annotation: 'Kitchan Design'
                },
                {
                    imgUrl: news2,
                    heading: 'Low Cost Latest Invented Interior DesigningIdeas.',
                    date: '22 December,2022',
                    annotation: 'Living Design'
                },
                {
                    imgUrl: news3,
                    heading: 'Best For Any Office & Business Interior Solution',
                    date: '25 December,2022',
                    annotation: 'Interior Design'
                },
                {
                    imgUrl: news4,
                    heading: 'Best For Any Office & Business Interior Solution',
                    date: '25 December,2022',
                    annotation: 'Kitchan Design'
                },
                {
                    imgUrl: news5,
                    heading: 'Best For Any Office & Business Interior Solution',
                    date: '25 December,2022',
                    annotation: 'Living Design'
                },
                {
                    imgUrl: news6,
                    heading: 'Best For Any Office & Business Interior Solution',
                    date: '25 December,2022',
                    annotation: 'Interior Design'
                },
            ]
        }
    }
  }
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style lang="scss">
    $widthSite: 1200px;
    $color-title: #292F36;
    $color-text: #4D5053;

    .center {
    padding-left: calc(50% - 600px);
    padding-right: calc(50% - 600px);
    }

    %flex-center{
        display: flex;
        align-items: center;
        justify-content: center;
    }

    %flex-center-x{
        display: flex;
        justify-content: center;
    }

    %flex-center-y{
        display: flex;
        align-items: center;
    }

    /* Blog */

.top-article{
    background-image: url('~@/assets/news-background.png');
    height: 365px;
    width: 100%;
    @extend %flex-center-x;
    align-items: flex-end;

    &__content{
        padding: 41px 78px;
        border-radius: 37px 37px 0px 0px;
        background: #FFF;
        @extend %flex-center-y;
        flex-direction: column;
    }

    &__heading{
        color: $color-title;
        font-family: DM Serif Display;
        font-size: 50px;
        line-height: 125%; 
    }

    &__breadcrumbs{
        display: flex;
    }

    &__li{
        color: $color-text;
        font-family: Jost;
        font-size: 22px;
        line-height: 150%; 
        letter-spacing: 0.22px
    }

    &__li:not(:last-child)::after{
        padding: 3px;
        color: $color-text;
        content: "\002F";
        padding-left: 8px;
        padding-right: 8px;
    }
}


/* Main */

.article-content{
    padding-top: 200px;
    padding-bottom: 200px;
}

.breadcrumbs{
    &__li{
        font-size: 22px;
        letter-spacing: 0.22px;
    }
}

/* Post */

.post{

    &__img{
        border-radius: 42px;
    }

    &__heading{
        color: $color-title;
        font-family: DM Serif Display;
        font-size: 50px;
        line-height: 125%; 
        letter-spacing: 1px;
        margin-bottom: 33px;
    }

    &__block{
        display: flex;
        padding: 22px;
        gap: 65px;
        border-radius: 62px;
        border: 1px solid #E7E7E7;
        box-shadow: 0px 10px 30px 0px rgba(255, 255, 255, 0.25);
    }

    &__content{
        padding-top: 50px;

        &_title{
            width: 463px;
            color: $color-title;
            font-family: DM Serif Display;
            font-size: 25px;
            line-height: 125%; 
            letter-spacing: 0.5px;
            margin-bottom: 22px;
        }

        &_text{
            width: 469px;
            color: $color-text;
            font-family: Jost;
            font-size: 22px;
            line-height: 150%; 
            letter-spacing: 0.22px;
            margin-bottom: 41px;
        }

        &_footer{
            @extend %flex-center-y;
            justify-content: space-between;
        }

        &_date{
            color: $color-text;
            font-family: Jost;
            font-size: 16px;
            line-height: 150%; 
            letter-spacing: 0.16px;
            text-transform: capitalize;
        }
    }
}

.news-blog{
    margin-top: 150px;
    margin-bottom: 30px;
}

.news__conteiner{
    @extend %flex-center-x;
}


.news{
    @extend %flex-center-y;
    flex-direction: column;

    &__heading{
        color: $color-title;
        font-family: DM Serif Display;
        font-size: 50px;
        line-height: 125%; 
        letter-spacing: 1px;
        margin-bottom: 12px;
    }

    &__text{
        width: 811px;
        color: $color-text;
        text-align: center;
        font-family: Jost;
        font-size: 22px;
        line-height: 150%; 
        letter-spacing: 0.22px;
        margin-bottom: 52px;
    }

    &__content{
        display: flex;
        flex-wrap: wrap;
        column-gap: 27px;
        row-gap: 30px;
    }

}


.pagination{
    margin-top: 51px;
    display: flex;
    gap: 20px;
    align-items: center;
}

  </style>