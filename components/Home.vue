<template>
    <div class="d-grid">
        <div class="header">
            <WebHeader />
        </div>
        <div class="body">
            <div class="slide-banner">
                <div class="d-flex mx-auto justify-content-between" style="padding: 0px 16px;">
                    <div class="">
                        <h2>Welcome back, ready for your next lessson?</h2>
                    </div>
                    <div class="">
                        <b-button variant="outline-primary" class="view-lesson">View lesson</b-button>
                    </div>
                </div>
                <div class="slide-lesson">
                    <div class="list-lessons">
                        <b-carousel id="carousel-1" v-model="slide" :interval="4000" controls indicators
                            background="#efeff7" img-width="1024" img-height="480"
                            style="text-shadow: 1px 1px 2px #333;" @sliding-start="onSlideStart"
                            @sliding-end="onSlideEnd">
                            <b-carousel-slide>
                                <template #img>
                                    <div class="d-flex lesson row">
                                        <div class="col-lg-6" style="background-color: #efeff7;">
                                            <div class="info-lesson mr-2 row">
                                                <div class="image-lesson col-lg-4">
                                                    <img class="d-block img-fluid" width="100%" height="150px"
                                                        :src="require(`~/assets/images/${listLesson[0].image}.png`)"
                                                        alt="image slot">
                                                </div>
                                                <div class="col-lg-8">
                                                    <div class="time-lesson">
                                                        <span>{{ listLesson[0].timeLesson }}</span>
                                                    </div>
                                                    <div class="title-lesson">
                                                        <h4>{{ listLesson[0].title }}</h4>
                                                    </div>
                                                    <div class="author-lesson">
                                                        <div class="ava-author">
                                                            <img :src="require(`~/assets/images/${listLesson[0].avatarAuthour}.png`)"
                                                                class="" alt="" />
                                                        </div>
                                                        <div class="name-author mx-2">
                                                            <span>{{ listLesson[0].author }}</span>
                                                        </div>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="col-lg-6 " style="background-color: #efeff7;">
                                            <div class="info-lesson ml-2 row">
                                                <div class="image-lesson col-lg-4">
                                                    <img class="d-block img-fluid" width="100%" height="150px"
                                                        :src="require(`~/assets/images/${listLesson[1].image}.png`)"
                                                        alt="image slot">
                                                </div>
                                                <div class="col-lg-8">
                                                    <div class="time-lesson">
                                                        <span>{{ listLesson[1].timeLesson }}</span>
                                                    </div>
                                                    <div class="title-lesson">
                                                        <h4>{{ listLesson[1].title }}</h4>
                                                    </div>
                                                    <div class="author-lesson">
                                                        <div class="ava-author">
                                                            <img :src="require(`~/assets/images/${listLesson[1].avatarAuthour}.png`)"
                                                                class="" alt="" />
                                                        </div>
                                                        <div class="name-author mx-2">
                                                            <span>{{ listLesson[1].author }}</span>
                                                        </div>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </template>
                            </b-carousel-slide>
                            <b-carousel-slide>
                                <template #img>
                                    <div class="d-flex lesson row">
                                        <div class="col-lg-6" style="background-color: #efeff7;">
                                            <div class="info-lesson mr-2 row">
                                                <div class="image-lesson col-lg-4">
                                                    <img class="d-block img-fluid" width="100%" height="150px"
                                                        :src="require(`~/assets/images/${listLesson[0].image}.png`)"
                                                        alt="image slot">
                                                </div>
                                                <div class="col-lg-8">
                                                    <div class="time-lesson">
                                                        <span>{{ listLesson[0].timeLesson }}</span>
                                                    </div>
                                                    <div class="title-lesson">
                                                        <h4>{{ listLesson[0].title }}</h4>
                                                    </div>
                                                    <div class="author-lesson">
                                                        <div class="ava-author">
                                                            <img :src="require(`~/assets/images/${listLesson[0].avatarAuthour}.png`)"
                                                                class="" alt="" />
                                                        </div>
                                                        <div class="name-author mx-2">
                                                            <span>{{ listLesson[0].author }}</span>
                                                        </div>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="col-lg-6" style="background-color: #efeff7;">
                                            <div class="info-lesson ml-2 row">
                                                <div class="image-lesson col-lg-4">
                                                    <img class="d-block img-fluid" width="100%" height="150px"
                                                        :src="require(`~/assets/images/${listLesson[1].image}.png`)"
                                                        alt="image slot">
                                                </div>
                                                <div class="col-lg-8">
                                                    <div class="time-lesson">
                                                        <span>{{ listLesson[1].timeLesson }}</span>
                                                    </div>
                                                    <div class="title-lesson">
                                                        <h4>{{ listLesson[1].title }}</h4>
                                                    </div>
                                                    <div class="author-lesson">
                                                        <div class="ava-author">
                                                            <img :src="require(`~/assets/images/${listLesson[1].avatarAuthour}.png`)"
                                                                class="" alt="" />
                                                        </div>
                                                        <div class="name-author mx-2">
                                                            <span>{{ listLesson[1].author }}</span>
                                                        </div>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </template>
                            </b-carousel-slide>
                            <b-carousel-slide>
                                <template #img>
                                    <div class="d-flex lesson row">
                                        <div class="col-lg-6" style="background-color: #efeff7;">
                                            <div class="info-lesson mr-2 row">
                                                <div class="image-lesson col-lg-4">
                                                    <img class="d-block img-fluid" width="100%" height="150px"
                                                        :src="require(`~/assets/images/${listLesson[0].image}.png`)"
                                                        alt="image slot">
                                                </div>
                                                <div class="col-lg-8">
                                                    <div class="time-lesson">
                                                        <span>{{ listLesson[0].timeLesson }}</span>
                                                    </div>
                                                    <div class="title-lesson">
                                                        <h4>{{ listLesson[0].title }}</h4>
                                                    </div>
                                                    <div class="author-lesson">
                                                        <div class="ava-author">
                                                            <img :src="require(`~/assets/images/${listLesson[0].avatarAuthour}.png`)"
                                                                class="" alt="" />
                                                        </div>
                                                        <div class="name-author mx-2">
                                                            <span>{{ listLesson[0].author }}</span>
                                                        </div>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="col-lg-6" style="background-color: #efeff7;">
                                            <div class="info-lesson ml-2 row">
                                                <div class="image-lesson col-lg-4">
                                                    <img class="d-block img-fluid" width="100%" height="150px"
                                                        :src="require(`~/assets/images/${listLesson[1].image}.png`)"
                                                        alt="image slot">
                                                </div>
                                                <div class="col-lg-8">
                                                    <div class="time-lesson">
                                                        <span>{{ listLesson[1].timeLesson }}</span>
                                                    </div>
                                                    <div class="title-lesson">
                                                        <h4>{{ listLesson[1].title }}</h4>
                                                    </div>
                                                    <div class="author-lesson">
                                                        <div class="ava-author">
                                                            <img :src="require(`~/assets/images/${listLesson[1].avatarAuthour}.png`)"
                                                                class="" alt="" />
                                                        </div>
                                                        <div class="name-author mx-2">
                                                            <span>{{ listLesson[1].author }}</span>
                                                        </div>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </template>
                            </b-carousel-slide>
                        </b-carousel>
                    </div>
                </div>
            </div>
            <div class="recommended">
                <div class="recommended-content d-flex mx-auto justify-content-between">
                    <div class="recommend-title">
                        <h2>Recommended For you</h2>
                    </div>
                    <div class="recommend-filter d-flex">
                        <div class="button-select mx-2">
                            <b-form-select v-model="selected" :options="options"
                                v-on:change="fillterTypeMusic(selected)"></b-form-select>
                        </div>
                        <div class="button-view ml-2">
                            <b-button variant="outline-danger" class="view-lesson">View all</b-button>
                        </div>
                    </div>
                </div>
                <div class="list-music row mx-0">
                    <div class="col-lg-4 my-3 " v-for="(item, index) in listMusic" v-bind:key="index">
                        <div class="info-music">
                            <div class="header-info">
                                <div class="music-image p-3">
                                    <img :src="require(`~/assets/images/${item.image}.png`)" class="" alt="" />
                                </div>
                                <div class="rate-music row mx-0 py-2">
                                    <div class="rating-music col-lg-4 col-sm-4 pr-0">
                                        <b-icon icon="star" class="icon-rating"></b-icon>
                                        <span>{{ item.rating }}</span>
                                    </div>
                                    <div class="view-music mx-0 col-lg-4 col-sm-4 pr-0">
                                        <b-icon icon="eye" class="icon-rating"></b-icon>
                                        <span>{{ item.eye }}</span>
                                    </div>
                                    <div class="listen-music mx-0 col-lg-4 col-sm-4 pr-0">
                                        <b-icon icon="play-circle" class="icon-rating"></b-icon>
                                        <span>{{ item.listen }}</span>
                                    </div>
                                </div>
                            </div>
                            <div class="author-music">
                                <div class="title-music">
                                    <h4>{{ item.title }}</h4>
                                </div>
                                <div class="info-author row">
                                    <div class="image-author col-lg-2 col-sm-2 pr-0">
                                        <img :src="require(`~/assets/images/${item.avatarAuthour}.png`)" class=""
                                            alt="" />
                                    </div>
                                    <div class="name-author col-lg-4 col-sm-4 px-0">
                                        <span>{{ item.author }}</span>
                                    </div>
                                    <div class="price-music col-lg-3 col-sm-3">
                                        <span>${{ item.promotionalPrice }}</span>
                                    </div>
                                    <div class="promo-price col-lg-3 col-sm-3">
                                        <span>${{ item.promotionalPrice }}</span>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="list-creators">
                <div class="header-list-creators">
                    <div class="title">
                        <h2>Classes Taught By Real Creators</h2>
                    </div>
                    <div class="button-view">
                        <b-button variant="outline-danger" class="view-lesson">View all</b-button>
                    </div>
                </div>
                <div class="row">
                    <div class="body-list-creators col-lg-4">
                        <div class="creator">
                            <div class="image-creator">
                                <div class="background-image-one">
                                </div>
                                <div class="ava-creator">
                                    <img src="@/assets/images/creator1.png">
                                </div>
                            </div>
                            <div class="body-creator py-4">
                                <div class="name-creator">
                                    <h3>Yamilet Booker</h3>
                                </div>
                                <div class="description-creator">
                                    Learn Adobe lllustrator CC grapphic design, logo design and more with in-depth,
                                    practical,
                                    easy-to-follow course!
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="body-list-creators col-lg-4">
                        <div class="creator">
                            <div class="image-creator">
                                <div class="background-image-two">
                                </div>
                                <div class="ava-creator">
                                    <img src="@/assets/images/creator2.png">
                                </div>
                            </div>
                            <div class="body-creator py-4">
                                <div class="name-creator">
                                    <h3>Aarav Lynn</h3>
                                </div>
                                <div class="description-creator">
                                    Learn Adobe lllustrator CC grapphic design, logo design and more with in-depth,
                                    practical,
                                    easy-to-follow course!
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="body-list-creators col-lg-4">
                        <div class="creator">
                            <div class="image-creator">
                                <div class="background-image-three">
                                </div>
                                <div class="ava-creator">
                                    <img src="@/assets/images/creator3.png">
                                </div>
                            </div>
                            <div class="body-creator py-4">
                                <div class="name-creator">
                                    <h3>Demetri Caron</h3>
                                </div>
                                <div class="description-creator">
                                    Learn Adobe lllustrator CC grapphic design, logo design and more with in-depth,
                                    practical,
                                    easy-to-follow course!
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="body-list-creators col-lg-4">
                        <div class="creator">
                            <div class="image-creator">
                                <div class="background-image-four">
                                </div>
                                <div class="ava-creator">
                                    <img src="@/assets/images/creator4.png">
                                </div>
                            </div>
                            <div class="body-creator py-4">
                                <div class="name-creator">
                                    <h3>Kiyan Dempsey</h3>
                                </div>
                                <div class="description-creator">
                                    Learn Adobe lllustrator CC grapphic design, logo design and more with in-depth,
                                    practical,
                                    easy-to-follow course!
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="body-list-creators col-lg-4">
                        <div class="creator">
                            <div class="image-creator">
                                <div class="background-image-five">
                                </div>
                                <div class="ava-creator">
                                    <img src="@/assets/images/creator5.png">
                                </div>
                            </div>
                            <div class="body-creator py-4">
                                <div class="name-creator">
                                    <h3>Nikky Engelen</h3>
                                </div>
                                <div class="description-creator">
                                    Learn Adobe lllustrator CC grapphic design, logo design and more with in-depth,
                                    practical,
                                    easy-to-follow course!
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="body-list-creators col-lg-4">
                        <div class="creator">
                            <div class="image-creator">
                                <div class="background-image-six">
                                </div>
                                <div class="ava-creator">
                                    <img src="@/assets/images/creator6.png">
                                </div>
                            </div>
                            <div class="body-creator py-4">
                                <div class="name-creator">
                                    <h3>Gracelyn Mason</h3>
                                </div>
                                <div class="description-creator">
                                    Learn Adobe lllustrator CC grapphic design, logo design and more with in-depth,
                                    practical,
                                    easy-to-follow course!
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="slogan">
                    <div class="row">
                        <div class="title-slogan col-lg-6">
                            <div class="text-slogan">
                                <span>I believe in lifelong learning and Skillfy is a great place to learn form expents.
                                    I've
                                    learned
                                    a lot and
                                    recommend it to all my friends.</span>
                            </div>
                            <div class="d-flex pt-3 text-author">
                                <span>
                                    Riaz suti
                                </span>
                                <div class="mx-2 straight-dash">
                                </div>
                                <span>
                                    Hearthy Foods
                                </span>
                            </div>
                        </div>
                        <div class="image-slogan col-lg-6 py-3">
                            <img src="@/assets/images/image_slogan.png">
                            <div class="icon-play">
                                <img src="@/assets/images/icon_play.png">
                            </div>
                            <!-- <iframe width="100%" height="100%"
                                src="https://www.youtube.com/embed/ZMpcWxmJy1U?si=o9MvK7MxIm5gLSi2"
                                title="YouTube video player" frameborder="0"
                                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                                referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe> -->
                        </div>
                    </div>
                </div>
            </div>
            <div class="choice-course">
                <div class="title-choice-course px-0">
                    <div class="title">
                        <h2>Get choice of your cource</h2>
                    </div>
                    <div class="button-view ml-2">
                        <b-button variant="outline-danger" class="view-lesson">View all</b-button>
                    </div>
                </div>
                <div class="list-lessons">
                    <b-carousel id="carousel-2" v-model="slide" :interval="4000" controls indicators
                        background="#efeff7" img-width="1024" img-height="480" style="text-shadow: 1px 1px 2px #333;"
                        @sliding-start="onSlideStart" @sliding-end="onSlideEnd">
                        <b-carousel-slide>
                            <template #img>
                                <div class="lesson row">
                                    <div class="info-music col-lg-4">
                                        <div class="header-info">
                                            <div class="music-image p-3">
                                                <img src="~/assets/images/nhac_kpop.png" class="" alt="" />
                                            </div>
                                            <div class="rate-music row mx-0 py-2">
                                                <div class="rating-music col-lg-4 pr-0">
                                                    <b-icon icon="star" class="icon-rating"></b-icon>
                                                    <span>4.5(120)</span>
                                                </div>
                                                <div class="view-music mx-0 col-lg-4 pr-0">
                                                    <b-icon icon="eye" class="icon-rating"></b-icon>
                                                    <span>28.500</span>
                                                </div>
                                                <div class="listen-music mx-0 col-lg-4 pr-0">
                                                    <b-icon icon="play-circle" class="icon-rating"></b-icon>
                                                    <span>36 Lesion</span>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="author-music">
                                            <div class="title-music">
                                                <h4>Everything You Need to Know About Business </h4>
                                            </div>
                                            <div class="info-author row">
                                                <div class="image-author col-lg-2 col-sm-2 pr-0">
                                                    <img src="~/assets/images/nhac2.png" class="" alt="" />
                                                </div>
                                                <div class="name-author col-lg-4 col-sm-4 px-0">
                                                    <span>Nicole Brown</span>
                                                </div>
                                                <div class="price-music col-lg-3 col-sm3">
                                                    <span>$99.99</span>
                                                </div>
                                                <div class="promo-price col-lg-3 col-sm-3">
                                                    <span>$49.99</span>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="info-music col-lg-4">
                                        <div class="header-info">
                                            <div class="music-image p-3">
                                                <img src="~/assets/images/nhac_jazz.png" class="" alt="" />
                                            </div>
                                            <div class="rate-music row mx-0 py-2">
                                                <div class="rating-music col-lg-4 pr-0">
                                                    <b-icon icon="star" class="icon-rating"></b-icon>
                                                    <span>4.5(120)</span>
                                                </div>
                                                <div class="view-music mx-0 col-lg-4 pr-0">
                                                    <b-icon icon="eye" class="icon-rating"></b-icon>
                                                    <span>28.500</span>
                                                </div>
                                                <div class="listen-music mx-0 col-lg-4 pr-0">
                                                    <b-icon icon="play-circle" class="icon-rating"></b-icon>
                                                    <span>36 Lesion</span>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="author-music">
                                            <div class="title-music">
                                                <h4>Everything You Need to Know About Business </h4>
                                            </div>
                                            <div class="info-author row">
                                                <div class="image-author col-lg-2 col-sm-2 pr-0">
                                                    <img src="~/assets/images/nhac2.png" class="" alt="" />
                                                </div>
                                                <div class="name-author col-lg-4 col-sm-4 px-0">
                                                    <span>Nicole Brown</span>
                                                </div>
                                                <div class="price-music col-lg-3 col-sm-3">
                                                    <span>$99.99</span>
                                                </div>
                                                <div class="promo-price col-lg-3 col-sm-3">
                                                    <span>$49.99</span>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="info-music col-lg-4">
                                        <div class="header-info">
                                            <div class="music-image p-3">
                                                <img src="~/assets/images/nhac_rap.png" class="" alt="" />
                                            </div>
                                            <div class="rate-music row mx-0 py-2">
                                                <div class="rating-music col-lg-4 pr-0">
                                                    <b-icon icon="star" class="icon-rating"></b-icon>
                                                    <span>4.5(120)</span>
                                                </div>
                                                <div class="view-music mx-0 col-lg-4 pr-0">
                                                    <b-icon icon="eye" class="icon-rating"></b-icon>
                                                    <span>28.500</span>
                                                </div>
                                                <div class="listen-music mx-0 col-lg-4 pr-0">
                                                    <b-icon icon="play-circle" class="icon-rating"></b-icon>
                                                    <span>36 Lesion</span>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="author-music">
                                            <div class="title-music">
                                                <h4>Everything You Need to Know About Business </h4>
                                            </div>
                                            <div class="info-author row">
                                                <div class="image-author col-lg-2 col-sm-2 pr-0">
                                                    <img src="~/assets/images/nhac2.png" class="" alt="" />
                                                </div>
                                                <div class="name-author col-lg-4 col-sm-4 px-0">
                                                    <span>Nicole Brown</span>
                                                </div>
                                                <div class="price-music col-lg-3 col-sm-3">
                                                    <span>$99.99</span>
                                                </div>
                                                <div class="promo-price col-lg-3 col-sm-3">
                                                    <span>$49.99</span>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </template>
                        </b-carousel-slide>
                        <b-carousel-slide>
                            <template #img>
                                <div class="lesson row">
                                    <div class="info-music col-lg-4">
                                        <div class="header-info">
                                            <div class="music-image p-3">
                                                <img src="~/assets/images/nhac_kpop.png" class="" alt="" />
                                            </div>
                                            <div class="rate-music row mx-0 py-2">
                                                <div class="rating-music col-lg-4 pr-0">
                                                    <b-icon icon="star" class="icon-rating"></b-icon>
                                                    <span>4.5(120)</span>
                                                </div>
                                                <div class="view-music mx-0 col-lg-4 pr-0">
                                                    <b-icon icon="eye" class="icon-rating"></b-icon>
                                                    <span>28.500</span>
                                                </div>
                                                <div class="listen-music mx-0 col-lg-4 pr-0">
                                                    <b-icon icon="play-circle" class="icon-rating"></b-icon>
                                                    <span>36 Lesion</span>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="author-music">
                                            <div class="title-music">
                                                <h4>Everything You Need to Know About Business </h4>
                                            </div>
                                            <div class="info-author row">
                                                <div class="image-author col-lg-2 col-sm-2 pr-0">
                                                    <img src="~/assets/images/nhac2.png" class="" alt="" />
                                                </div>
                                                <div class="name-author col-lg-4 col-sm-4 px-0">
                                                    <span>Nicole Brown</span>
                                                </div>
                                                <div class="price-music col-lg-3 col-sm-3">
                                                    <span>$99.99</span>
                                                </div>
                                                <div class="promo-price col-lg-3 col-sm-3">
                                                    <span>$49.99</span>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="info-music col-lg-4">
                                        <div class="header-info">
                                            <div class="music-image p-3">
                                                <img src="~/assets/images/nhac_jazz.png" class="" alt="" />
                                            </div>
                                            <div class="rate-music row mx-0 py-2">
                                                <div class="rating-music col-lg-4 pr-0">
                                                    <b-icon icon="star" class="icon-rating"></b-icon>
                                                    <span>4.5(120)</span>
                                                </div>
                                                <div class="view-music mx-0 col-lg-4 pr-0">
                                                    <b-icon icon="eye" class="icon-rating"></b-icon>
                                                    <span>28.500</span>
                                                </div>
                                                <div class="listen-music mx-0 col-lg-4 pr-0">
                                                    <b-icon icon="play-circle" class="icon-rating"></b-icon>
                                                    <span>36 Lesion</span>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="author-music">
                                            <div class="title-music">
                                                <h4>Everything You Need to Know About Business </h4>
                                            </div>
                                            <div class="info-author row">
                                                <div class="image-author col-lg-2 col-sm-2 pr-0">
                                                    <img src="~/assets/images/nhac2.png" class="" alt="" />
                                                </div>
                                                <div class="name-author col-lg-4 col-sm-4 px-0">
                                                    <span>Nicole Brown</span>
                                                </div>
                                                <div class="price-music col-lg-3 col-sm-3">
                                                    <span>$99.99</span>
                                                </div>
                                                <div class="promo-price col-lg-3 col-sm-3">
                                                    <span>$49.99</span>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="info-music col-lg-4">
                                        <div class="header-info">
                                            <div class="music-image p-3">
                                                <img src="~/assets/images/nhac_rap.png" class="" alt="" />
                                            </div>
                                            <div class="rate-music row mx-0 py-2">
                                                <div class="rating-music col-lg-4 pr-0">
                                                    <b-icon icon="star" class="icon-rating"></b-icon>
                                                    <span>4.5(120)</span>
                                                </div>
                                                <div class="view-music mx-0 col-lg-4 pr-0">
                                                    <b-icon icon="eye" class="icon-rating"></b-icon>
                                                    <span>28.500</span>
                                                </div>
                                                <div class="listen-music mx-0 col-lg-4 pr-0">
                                                    <b-icon icon="play-circle" class="icon-rating"></b-icon>
                                                    <span>36 Lesion</span>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="author-music">
                                            <div class="title-music">
                                                <h4>Everything You Need to Know About Business </h4>
                                            </div>
                                            <div class="info-author row">
                                                <div class="image-author col-lg-2 col-sm-2 pr-0">
                                                    <img src="~/assets/images/nhac2.png" class="" alt="" />
                                                </div>
                                                <div class="name-author col-lg-4 col-sm-4 px-0">
                                                    <span>Nicole Brown</span>
                                                </div>
                                                <div class="price-music col-lg-3 col-sm-3">
                                                    <span>$99.99</span>
                                                </div>
                                                <div class="promo-price col-lg-3 col-sm-3">
                                                    <span>$49.99</span>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </template>
                        </b-carousel-slide>
                        <b-carousel-slide>
                            <template #img>
                                <div class="lesson row">
                                    <div class="info-music col-lg-4">
                                        <div class="header-info">
                                            <div class="music-image p-3">
                                                <img src="~/assets/images/nhac_kpop.png" class="" alt="" />
                                            </div>
                                            <div class="rate-music row mx-0 py-2">
                                                <div class="rating-music col-lg-4 pr-0">
                                                    <b-icon icon="star" class="icon-rating"></b-icon>
                                                    <span>4.5(120)</span>
                                                </div>
                                                <div class="view-music mx-0 col-lg-4 pr-0">
                                                    <b-icon icon="eye" class="icon-rating"></b-icon>
                                                    <span>28.500</span>
                                                </div>
                                                <div class="listen-music mx-0 col-lg-4 pr-0">
                                                    <b-icon icon="play-circle" class="icon-rating"></b-icon>
                                                    <span>36 Lesion</span>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="author-music">
                                            <div class="title-music">
                                                <h4>Everything You Need to Know About Business </h4>
                                            </div>
                                            <div class="info-author row">
                                                <div class="image-author col-lg-2 col-sm-2 pr-0">
                                                    <img src="~/assets/images/nhac2.png" class="" alt="" />
                                                </div>
                                                <div class="name-author col-lg-4 col-sm-4 px-0">
                                                    <span>Nicole Brown</span>
                                                </div>
                                                <div class="price-music col-lg-3 col-sm-3">
                                                    <span>$99.99</span>
                                                </div>
                                                <div class="promo-price col-lg-3 col-sm-3">
                                                    <span>$49.99</span>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="info-music col-lg-4">
                                        <div class="header-info">
                                            <div class="music-image p-3">
                                                <img src="~/assets/images/nhac_jazz.png" class="" alt="" />
                                            </div>
                                            <div class="rate-music row mx-0 py-2">
                                                <div class="rating-music col-lg-4 pr-0">
                                                    <b-icon icon="star" class="icon-rating"></b-icon>
                                                    <span>4.5(120)</span>
                                                </div>
                                                <div class="view-music mx-0 col-lg-4 pr-0">
                                                    <b-icon icon="eye" class="icon-rating"></b-icon>
                                                    <span>28.500</span>
                                                </div>
                                                <div class="listen-music mx-0 col-lg-4 pr-0">
                                                    <b-icon icon="play-circle" class="icon-rating"></b-icon>
                                                    <span>36 Lesion</span>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="author-music">
                                            <div class="title-music">
                                                <h4>Everything You Need to Know About Business </h4>
                                            </div>
                                            <div class="info-author row">
                                                <div class="image-author col-lg-2 col-sm-2 pr-0">
                                                    <img src="~/assets/images/nhac2.png" class="" alt="" />
                                                </div>
                                                <div class="name-author col-lg-4 col-sm-4 px-0">
                                                    <span>Nicole Brown</span>
                                                </div>
                                                <div class="price-music col-lg-3 col-sm-3">
                                                    <span>$99.99</span>
                                                </div>
                                                <div class="promo-price col-lg-3 col-sm-3">
                                                    <span>$49.99</span>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="info-music col-lg-4">
                                        <div class="header-info">
                                            <div class="music-image p-3">
                                                <img src="~/assets/images/nhac_rap.png" class="" alt="" />
                                            </div>
                                            <div class="rate-music row mx-0 py-2">
                                                <div class="rating-music col-lg-4 pr-0">
                                                    <b-icon icon="star" class="icon-rating"></b-icon>
                                                    <span>4.5(120)</span>
                                                </div>
                                                <div class="view-music mx-0 col-lg-4 pr-0">
                                                    <b-icon icon="eye" class="icon-rating"></b-icon>
                                                    <span>28.500</span>
                                                </div>
                                                <div class="listen-music mx-0 col-lg-4 pr-0">
                                                    <b-icon icon="play-circle" class="icon-rating"></b-icon>
                                                    <span>36 Lesion</span>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="author-music">
                                            <div class="title-music">
                                                <h4>Everything You Need to Know About Business </h4>
                                            </div>
                                            <div class="info-author row">
                                                <div class="image-author col-lg-2 col-sm-2 pr-0">
                                                    <img src="~/assets/images/nhac2.png" class="" alt="" />
                                                </div>
                                                <div class="name-author col-lg-4 col-sm-4 px-0">
                                                    <span>Nicole Brown</span>
                                                </div>
                                                <div class="price-music col-lg-3 col-sm-3">
                                                    <span>$99.99</span>
                                                </div>
                                                <div class="promo-price col-lg-3 col-sm-3">
                                                    <span>$49.99</span>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </template>
                        </b-carousel-slide>
                        <b-carousel-slide>
                            <template #img>
                                <div class="lesson row">
                                    <div class="info-music col-lg-4">
                                        <div class="header-info">
                                            <div class="music-image p-3">
                                                <img src="~/assets/images/nhac_kpop.png" class="" alt="" />
                                            </div>
                                            <div class="rate-music row mx-0 py-2">
                                                <div class="rating-music col-lg-4 pr-0">
                                                    <b-icon icon="star" class="icon-rating"></b-icon>
                                                    <span>4.5(120)</span>
                                                </div>
                                                <div class="view-music mx-0 col-lg-4 pr-0">
                                                    <b-icon icon="eye" class="icon-rating"></b-icon>
                                                    <span>28.500</span>
                                                </div>
                                                <div class="listen-music mx-0 col-lg-4 pr-0">
                                                    <b-icon icon="play-circle" class="icon-rating"></b-icon>
                                                    <span>36 Lesion</span>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="author-music">
                                            <div class="title-music">
                                                <h4>Everything You Need to Know About Business </h4>
                                            </div>
                                            <div class="info-author row">
                                                <div class="image-author col-lg-2 col-sm-2 pr-0">
                                                    <img src="~/assets/images/nhac2.png" class="" alt="" />
                                                </div>
                                                <div class="name-author col-lg-4 col-sm-4 px-0">
                                                    <span>Nicole Brown</span>
                                                </div>
                                                <div class="price-music col-lg-3 col-sm-3">
                                                    <span>$99.99</span>
                                                </div>
                                                <div class="promo-price col-lg-3 col-sm-3">
                                                    <span>$49.99</span>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="info-music col-lg-4">
                                        <div class="header-info">
                                            <div class="music-image p-3">
                                                <img src="~/assets/images/nhac_jazz.png" class="" alt="" />
                                            </div>
                                            <div class="rate-music row mx-0 py-2">
                                                <div class="rating-music col-lg-4 pr-0">
                                                    <b-icon icon="star" class="icon-rating"></b-icon>
                                                    <span>4.5(120)</span>
                                                </div>
                                                <div class="view-music mx-0 col-lg-4 pr-0">
                                                    <b-icon icon="eye" class="icon-rating"></b-icon>
                                                    <span>28.500</span>
                                                </div>
                                                <div class="listen-music mx-0 col-lg-4 pr-0">
                                                    <b-icon icon="play-circle" class="icon-rating"></b-icon>
                                                    <span>36 Lesion</span>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="author-music">
                                            <div class="title-music">
                                                <h4>Everything You Need to Know About Business </h4>
                                            </div>
                                            <div class="info-author row">
                                                <div class="image-author col-lg-2 col-sm-2 pr-0">
                                                    <img src="~/assets/images/nhac2.png" class="" alt="" />
                                                </div>
                                                <div class="name-author col-lg-4 col-sm-4 px-0">
                                                    <span>Nicole Brown</span>
                                                </div>
                                                <div class="price-music col-lg-3 col-sm-3">
                                                    <span>$99.99</span>
                                                </div>
                                                <div class="promo-price col-lg-3 col-sm-3">
                                                    <span>$49.99</span>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="info-music col-lg-4">
                                        <div class="header-info">
                                            <div class="music-image p-3">
                                                <img src="~/assets/images/nhac_rap.png" class="" alt="" />
                                            </div>
                                            <div class="rate-music row mx-0 py-2">
                                                <div class="rating-music col-lg-4 pr-0">
                                                    <b-icon icon="star" class="icon-rating"></b-icon>
                                                    <span>4.5(120)</span>
                                                </div>
                                                <div class="view-music mx-0 col-lg-4 pr-0">
                                                    <b-icon icon="eye" class="icon-rating"></b-icon>
                                                    <span>28.500</span>
                                                </div>
                                                <div class="listen-music mx-0 col-lg-4 pr-0">
                                                    <b-icon icon="play-circle" class="icon-rating"></b-icon>
                                                    <span>36 Lesion</span>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="author-music">
                                            <div class="title-music">
                                                <h4>Everything You Need to Know About Business </h4>
                                            </div>
                                            <div class="info-author row">
                                                <div class="image-author col-lg-2 col-sm-2 pr-0">
                                                    <img src="~/assets/images/nhac2.png" class="" alt="" />
                                                </div>
                                                <div class="name-author col-lg-4 col-sm-4 px-0">
                                                    <span>Nicole Brown</span>
                                                </div>
                                                <div class="price-music col-lg-3 col-sm-3">
                                                    <span>$99.99</span>
                                                </div>
                                                <div class="promo-price col-lg-3 col-sm-3">
                                                    <span>$49.99</span>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </template>
                        </b-carousel-slide>
                    </b-carousel>
                </div>
            </div>
            <div class="favorite-course">
                <div class="header-favorite-course">
                    <div class="title">
                        <h2>Choice favorite cource from top category</h2>
                    </div>
                    <div class="button-see">
                        <b-button variant="outline-danger" class="view-lesson">See all Category</b-button>
                    </div>
                </div>
                <div class="body-favorite-course my-3">
                    <div class="list-course row mx-0">
                        <div class="info-course-1 my-3 col-lg-3 w-100">
                            <div class="background-course">
                                <div class="d-grid py-3 px-2">
                                    <b-icon font-scale="3" icon="pen" class="border border-info rounded"
                                        variant="info"></b-icon>
                                    <div class="title-course py-2">
                                        <h3>Design</h3>
                                    </div>
                                    <div class="description-course">
                                        Learn Adobe IIIlusator CC graphic design, logo design, and more with this
                                        in-depth,
                                        practical,
                                        easy~
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="info-course-2  my-3 col-lg-3 w-100">
                            <div class="background-course">
                                <div class="d-grid py-3 px-2">
                                    <b-icon font-scale="3" icon="tv" class="border border-info rounded"
                                        variant="info"></b-icon>
                                    <div class="title-course py-2">
                                        <h3>Development</h3>
                                    </div>
                                    <div class="description-course">
                                        Learn Adobe IIIlusator CC graphic design, logo design, and more with this
                                        in-depth,
                                        practical,
                                        easy~
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="info-course-3 my-3 col-lg-3 w-100">
                            <div class="background-course">
                                <div class="d-grid py-3 px-2">
                                    <b-icon font-scale="3" icon="layout-text-sidebar" class="border border-info rounded"
                                        variant="info"></b-icon>
                                    <div class="title-course py-2">
                                        <h3>Development</h3>
                                    </div>
                                    <div class="description-course">
                                        Learn Adobe IIIlusator CC graphic design, logo design, and more with this
                                        in-depth,
                                        practical,
                                        easy~
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="info-course-4 my-3 col-lg-3 w-100">
                            <div class="background-course">
                                <div class="d-grid py-3 px-2">
                                    <b-icon font-scale="3" icon="layout-text-sidebar" class="border border-info rounded"
                                        variant="info"></b-icon>
                                    <div class="title-course py-2">
                                        <h3>Development</h3>
                                    </div>
                                    <div class="description-course">
                                        Learn Adobe IIIlusator CC graphic design, logo design, and more with this
                                        in-depth,
                                        practical,
                                        easy~
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="online-coaching-lessons">
                <div class="title py-3">
                    <h2>Online Coaching Lessons For Remote Learning.</h2>
                </div>
                <div class="description py-3">
                    <span>100% online learning from the world's best universities and companies</span>
                </div>
                <div class="button-join py-3">
                    <b-button variant="outline-primary" class="view-lesson">Join Today</b-button>
                </div>
            </div>
            <div class="top-education">
                <div class="title-top-education px-0">
                    <div class="title">
                        <h2>Top Education offers and deals are listed here</h2>
                    </div>
                    <div class="button-view ml-2">
                        <b-button variant="outline-danger" class="view-lesson">View all</b-button>
                    </div>
                </div>
                <div class="list-offer-educations mt-5">
                    <b-carousel id="carousel-3" v-model="slide" :interval="4000" controls indicators
                        background="#efeff7" img-width="1024" img-height="480" style="text-shadow: 1px 1px 2px black;"
                        @sliding-start="onSlideStart" @sliding-end="onSlideEnd">
                        <b-carousel-slide>
                            <template #img>
                                <div class="row">
                                    <div class="job-education col-lg-4">
                                        <div class="offer-education-1 h-100 ml-3">
                                            <div class="background-offer-education">
                                            </div>
                                            <div class="row h-100">
                                                <div class="info-offer-education col-lg-6">
                                                    <div class="title-discount px-0">
                                                        <span>Up To 58% Off</span>
                                                    </div>
                                                    <div class="title-offer pt-3">
                                                        <span>Get 12-Month Subscription</span>
                                                    </div>
                                                    <div class="total-discount">
                                                        <div class="text-discount">
                                                            Total Discount
                                                        </div>
                                                        <div class="number-discount">
                                                            50%
                                                        </div>
                                                    </div>
                                                </div>
                                                <div class="image-offer-education col-lg-6">
                                                    <img src="@/assets/images/creator1.png">
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="job-education col-lg-4">
                                        <div class="offer-education-2 h-100 ml-3">
                                            <div class="background-offer-education">
                                            </div>
                                            <div class="row h-100">
                                                <div class="info-offer-education col-lg-6">
                                                    <div class="title-discount px-0">
                                                        <span>Productvity Cource </span>
                                                    </div>
                                                    <div class="title-offer pt-3">
                                                        <span>The Complete Personal</span>
                                                    </div>
                                                    <div class="total-discount">
                                                        <div class="text-discount">
                                                            Up To 58% Off
                                                        </div>
                                                        <div class="number-discount">
                                                            58%
                                                        </div>
                                                    </div>
                                                </div>
                                                <div class="image-offer-education col-lg-6">
                                                    <img src="@/assets/images/creator3.png">
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="job-education col-lg-4">
                                        <div class="offer-education-3 h-100 ml-3">
                                            <div class="background-offer-education">
                                            </div>
                                            <div class="row h-100">
                                                <div class="info-offer-education col-lg-6">
                                                    <div class="title-discount px-0">
                                                        <span>Pass above Rs 250.</span>
                                                    </div>
                                                    <div class="title-offer pt-3">
                                                        <span>Avail 10% off on Testbook</span>
                                                    </div>
                                                    <div class="total-discount">
                                                        <div class="text-discount">
                                                            Total Discount
                                                        </div>
                                                        <div class="number-discount">
                                                            10%
                                                        </div>
                                                    </div>
                                                </div>
                                                <div class="image-offer-education col-lg-6">
                                                    <img src="@/assets/images/creator4.png">
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </template>
                        </b-carousel-slide>
                        <b-carousel-slide>
                            <template #img>
                                <div class="row">
                                    <div class="job-education col-lg-4">
                                        <div class="offer-education-1 h-100 ml-3">
                                            <div class="background-offer-education">
                                            </div>
                                            <div class="row h-100">
                                                <div class="info-offer-education col-lg-6">
                                                    <div class="title-discount px-0">
                                                        <span>Up To 58% Off</span>
                                                    </div>
                                                    <div class="title-offer pt-3">
                                                        <span>Get 12-Month Subscription</span>
                                                    </div>
                                                    <div class="total-discount">
                                                        <div class="text-discount">
                                                            Total Discount
                                                        </div>
                                                        <div class="number-discount">
                                                            50%
                                                        </div>
                                                    </div>
                                                </div>
                                                <div class="image-offer-education col-lg-6">
                                                    <img src="@/assets/images/creator1.png">
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="job-education col-lg-4">
                                        <div class="offer-education-2 h-100 ml-3">
                                            <div class="background-offer-education">
                                            </div>
                                            <div class="row h-100">
                                                <div class="info-offer-education col-lg-6">
                                                    <div class="title-discount px-0">
                                                        <span>Productvity Cource </span>
                                                    </div>
                                                    <div class="title-offer pt-3">
                                                        <span>The Complete Personal</span>
                                                    </div>
                                                    <div class="total-discount">
                                                        <div class="text-discount">
                                                            Up To 58% Off
                                                        </div>
                                                        <div class="number-discount">
                                                            58%
                                                        </div>
                                                    </div>
                                                </div>
                                                <div class="image-offer-education col-lg-6">
                                                    <img src="@/assets/images/creator3.png">
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="job-education col-lg-4">
                                        <div class="offer-education-3 h-100 ml-3">
                                            <div class="background-offer-education">
                                            </div>
                                            <div class="row h-100">
                                                <div class="info-offer-education col-lg-6">
                                                    <div class="title-discount px-0">
                                                        <span>Pass above Rs 250.</span>
                                                    </div>
                                                    <div class="title-offer pt-3">
                                                        <span>Avail 10% off on Testbook</span>
                                                    </div>
                                                    <div class="total-discount">
                                                        <div class="text-discount">
                                                            Total Discount
                                                        </div>
                                                        <div class="number-discount">
                                                            10%
                                                        </div>
                                                    </div>
                                                </div>
                                                <div class="image-offer-education col-lg-6">
                                                    <img src="@/assets/images/creator4.png">
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </template>
                        </b-carousel-slide>
                        <b-carousel-slide>
                            <template #img>
                                <div class="row">
                                    <div class="job-education col-lg-4">
                                        <div class="offer-education-1 h-100 ml-3">
                                            <div class="background-offer-education">
                                            </div>
                                            <div class="row h-100">
                                                <div class="info-offer-education col-lg-6">
                                                    <div class="title-discount px-0">
                                                        <span>Up To 58% Off</span>
                                                    </div>
                                                    <div class="title-offer pt-3">
                                                        <span>Get 12-Month Subscription</span>
                                                    </div>
                                                    <div class="total-discount">
                                                        <div class="text-discount">
                                                            Total Discount
                                                        </div>
                                                        <div class="number-discount">
                                                            50%
                                                        </div>
                                                    </div>
                                                </div>
                                                <div class="image-offer-education col-lg-6">
                                                    <img src="@/assets/images/creator1.png">
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="job-education col-lg-4">
                                        <div class="offer-education-2 h-100 ml-3">
                                            <div class="background-offer-education">
                                            </div>
                                            <div class="row h-100">
                                                <div class="info-offer-education col-lg-6">
                                                    <div class="title-discount px-0">
                                                        <span>Productvity Cource </span>
                                                    </div>
                                                    <div class="title-offer pt-3">
                                                        <span>The Complete Personal</span>
                                                    </div>
                                                    <div class="total-discount">
                                                        <div class="text-discount">
                                                            Up To 58% Off
                                                        </div>
                                                        <div class="number-discount">
                                                            58%
                                                        </div>
                                                    </div>
                                                </div>
                                                <div class="image-offer-education col-lg-6">
                                                    <img src="@/assets/images/creator3.png">
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="job-education col-lg-4">
                                        <div class="offer-education-3 h-100 ml-3">
                                            <div class="background-offer-education">
                                            </div>
                                            <div class="row h-100">
                                                <div class="info-offer-education col-lg-6">
                                                    <div class="title-discount px-0">
                                                        <span>Pass above Rs 250.</span>
                                                    </div>
                                                    <div class="title-offer pt-3">
                                                        <span>Avail 10% off on Testbook</span>
                                                    </div>
                                                    <div class="total-discount">
                                                        <div class="text-discount">
                                                            Total Discount
                                                        </div>
                                                        <div class="number-discount">
                                                            10%
                                                        </div>
                                                    </div>
                                                </div>
                                                <div class="image-offer-education col-lg-6">
                                                    <img src="@/assets/images/creator4.png">
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </template>
                        </b-carousel-slide>
                        <b-carousel-slide>
                            <template #img>
                                <div class="row">
                                    <div class="job-education col-lg-4">
                                        <div class="offer-education-1 h-100 ml-3">
                                            <div class="background-offer-education">
                                            </div>
                                            <div class="row h-100">
                                                <div class="info-offer-education col-lg-6">
                                                    <div class="title-discount px-0">
                                                        <span>Up To 58% Off</span>
                                                    </div>
                                                    <div class="title-offer pt-3">
                                                        <span>Get 12-Month Subscription</span>
                                                    </div>
                                                    <div class="total-discount">
                                                        <div class="text-discount">
                                                            Total Discount
                                                        </div>
                                                        <div class="number-discount">
                                                            50%
                                                        </div>
                                                    </div>
                                                </div>
                                                <div class="image-offer-education col-lg-6">
                                                    <img src="@/assets/images/creator1.png">
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="job-education col-lg-4">
                                        <div class="offer-education-2 h-100 ml-3">
                                            <div class="background-offer-education">
                                            </div>
                                            <div class="row h-100">
                                                <div class="info-offer-education col-lg-6">
                                                    <div class="title-discount px-0">
                                                        <span>Productvity Cource </span>
                                                    </div>
                                                    <div class="title-offer pt-3">
                                                        <span>The Complete Personal</span>
                                                    </div>
                                                    <div class="total-discount">
                                                        <div class="text-discount">
                                                            Up To 58% Off
                                                        </div>
                                                        <div class="number-discount">
                                                            58%
                                                        </div>
                                                    </div>
                                                </div>
                                                <div class="image-offer-education col-lg-6">
                                                    <img src="@/assets/images/creator3.png">
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="job-education col-lg-4">
                                        <div class="offer-education-3 h-100 ml-3">
                                            <div class="background-offer-education">
                                            </div>
                                            <div class="row h-100">
                                                <div class="info-offer-education col-lg-6">
                                                    <div class="title-discount px-0">
                                                        <span>Pass above Rs 250.</span>
                                                    </div>
                                                    <div class="title-offer pt-3">
                                                        <span>Avail 10% off on Testbook</span>
                                                    </div>
                                                    <div class="total-discount">
                                                        <div class="text-discount">
                                                            Total Discount
                                                        </div>
                                                        <div class="number-discount">
                                                            10%
                                                        </div>
                                                    </div>
                                                </div>
                                                <div class="image-offer-education col-lg-6">
                                                    <img src="@/assets/images/creator4.png">
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </template>
                        </b-carousel-slide>
                    </b-carousel>
                </div>
            </div>
        </div>
        <div class="footer">
            <WebFooter />
        </div>
    </div>
</template>

<script>

import WebHeader from '@/components/HeaderPage';
import WebFooter from '@/components/FooterPage';

export default {
    name: 'HomePage',
    components: { WebHeader, WebFooter },
    data() {
        return {
            slide: 0,
            sliding: null,
            options: [
                { value: null, text: 'All Lesson' },
                { value: 'kpop', text: 'KPop' },
                { value: 'jazz', text: 'Jazz' },
                { value: 'rock', text: 'Rock' },
                { value: 'rap', text: 'Rap' },
                { value: 'edm', text: 'EDM' }
            ],
            selected: null,
            listLesson: [
                {
                    image: 'nhac1',
                    title: 'Mer Duplicater in Sketch- Inconsistent Symbols & Styles',
                    avatarAuthour: 'nhac2',
                    author: 'Nice Brown',
                    timeLesson: '20/11/2011'
                },
                {
                    image: 'nhac1',
                    title: 'Mer Duplicater in Sketch- Inconsistent Symbols & Styles',
                    avatarAuthour: 'nhac2',
                    author: 'Nice Brown',
                    timeLesson: '20/11/2011'
                },
                {
                    image: 'nhac1',
                    title: 'Mer Duplicater in Sketch- Inconsistent Symbols & Styles',
                    avatarAuthour: 'nhac2',
                    author: 'Nice Brown',
                    timeLesson: '20/11/2011'
                },
                {
                    image: 'nhac1',
                    title: 'Mer Duplicater in Sketch- Inconsistent Symbols & Styles',
                    avatarAuthour: 'nhac2',
                    author: 'Nice Brown',
                    timeLesson: '20/11/2011'
                },
                {
                    image: 'nhac1',
                    title: 'Mer Duplicater in Sketch- Inconsistent Symbols & Styles',
                    avatarAuthour: 'nhac2',
                    author: 'Nice Brown',
                    timeLesson: '20/11/2011'
                },
                {
                    image: 'nhac1',
                    title: 'Mer Duplicater in Sketch- Inconsistent Symbols & Styles',
                    avatarAuthour: 'nhac2',
                    author: 'Nice Brown',
                    timeLesson: '20/11/2011'
                }

            ],
            listDataMusic: [
                {
                    image: 'nhac_kpop',
                    title: 'Mer Duplicater in Sketch- Inconsistent Symbols & Styles',
                    avatarAuthour: 'nhac2',
                    author: 'Nice Brown',
                    rating: '4.5(120)',
                    eye: '28,500',
                    listen: '36 Lesion',
                    price: '$99.99',
                    promotionalPrice: '49.65',
                    type: 'kpop'
                },
                {
                    image: 'nhac_1',
                    title: 'Mer Duplicater in Sketch- Inconsistent Symbols & Styles',
                    avatarAuthour: 'nhac2',
                    author: 'Nice Brown',
                    rating: '4.5(120)',
                    eye: '28,500',
                    listen: '36 Lesion',
                    price: '$99.99',
                    promotionalPrice: '49.65',
                    type: 'edm'
                },
                {
                    image: 'nhac_jazz',
                    title: 'Mer Duplicater in Sketch- Inconsistent Symbols & Styles',
                    avatarAuthour: 'nhac2',
                    author: 'Nice Brown',
                    rating: '4.5(120)',
                    eye: '28,500',
                    listen: '36 Lesion',
                    price: '$99.99',
                    promotionalPrice: '49.65',
                    type: 'jazz'
                },
                {
                    image: 'nhac_rock',
                    title: 'Mer Duplicater in Sketch- Inconsistent Symbols & Styles',
                    avatarAuthour: 'nhac2',
                    author: 'Nice Brown',
                    rating: '4.5(120)',
                    eye: '28,500',
                    listen: '36 Lesion',
                    price: '$99.99',
                    promotionalPrice: '49.65',
                    type: 'rock'
                },
                {
                    image: 'nhac_rap',
                    title: 'Mer Duplicater in Sketch- Inconsistent Symbols & Styles',
                    avatarAuthour: 'nhac2',
                    author: 'Nice Brown',
                    rating: '4.5(120)',
                    eye: '28,500',
                    listen: '36 Lesion',
                    price: '$99.99',
                    promotionalPrice: '49.65',
                    type: 'rap'
                },
                {
                    image: 'nhac_pop',
                    title: 'Mer Duplicater in Sketch- Inconsistent Symbols & Styles',
                    avatarAuthour: 'nhac2',
                    author: 'Nice Brown',
                    rating: '4.5(120)',
                    eye: '28,500',
                    listen: '36 Lesion',
                    price: '$99.99',
                    promotionalPrice: '49.65',
                    type: 'kpop'
                }
            ],
            listMusic: [],
        }
    },
    created() {
        this.listMusic = this.listDataMusic;
    },
    methods: {
        onSlideStart(slide) {
            this.sliding = true
        },
        onSlideEnd(slide) {
            this.sliding = false
        },
        fillterTypeMusic(selected) {
            const listNewMusic = [];
            if (selected !== null) {
                this.listDataMusic.forEach((element) => {
                    if (element.type === selected) {
                        listNewMusic.push(element)
                        this.listMusic = listNewMusic;
                    }
                })
            } else {
                this.listMusic = this.listDataMusic;
            }

        }
    }
}

</script>
<style>
@import '~/assets/scss/home/home.scss';
</style>