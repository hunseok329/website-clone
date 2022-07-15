<template>
    <div class="home-page">
        <div class="container home-header">
            <div class="row">
                <div class="home_headder-wrap">
                    <div class="home-header__story">
                        <div class="story__image-wrap">
                            <img class="story__image" src="../../assets/165589363178178969.webp" aria-label="home-page-img">
                        </div>
                        <div class="story__content-wrap">
                            <div class="story__content">
                                <div class="story__content__title">
                                    체리 몰딩과 화이트가 공존하는 두 얼굴의 신혼집
                                    <br>
                                </div>
                                <div class="story__content__profile">
                                    <img src="../../assets/free-icon-user-847969.png">
                                    <span>hunseok329</span>
                                </div>
                            </div>
                            <div class="story__content__more">보러가기</div>
                        </div>
                    </div>
                </div>
                <div class="home_headder-wrap-sub">
                    <div class="home_hearder__sub">
                        <div class="story__imdage-subwrap">
                            <img class="story__image-sub" src="../../assets/sign_up_web_v2.webp">
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CommunityHome',
}
</script>

<style>
    .home-page {
        display: flex;
        flex-direction: column;
    }
    .home-header {
        padding: 30px 0 0;
    }
    .container {
        box-sizing: border-box;
        margin: 0 auto;
        max-width: 100%;
        width: 1136px;
    }
    .row {
        display: flex;
        box-sizing: border-box;
        align-items: stretch;
        flex-wrap: wrap;

    }
    .home_headder-wrap {
        padding-right: 10px;
        padding-left: 10px;
        width: 100%;
        box-sizing: border-box;
        position: relative;
        flex: 0 0 75%;
    }
    .home-header__story {
        position: relative;
        display: block;
        box-sizing: border-box;
    }
    .story__image-wrap {
        box-sizing: border-box;       

    }
    .story__image {
        top: 50%;
        left: 50%;
        width: 100%;
        min-height: 100%;
        border-radius: 6px; 
    }
    .story__content-wrap {
        display: flex;
        padding: 40px;
        position: absolute;
        align-items: flex-end;
        left: 0;
        right: 0;
        top: 0;
        bottom: 0;
        z-index: 2;
        flex: 1 1 0px;
    }
    .story__content {
        flex: 1 1 0px;
        color: #fff;
        font-weight: 700;
    }
    .story__content__title {
        max-height: 88px;
        font-size: 32px;
        margin: 8px 0 10px;
        line-height: 1.38;
    }
    .story__content__profile {
        display: block;
        font-size: 13px;
        font-weight: 400;
        white-space: nowrap;
    }
    .story__content__more {
        width: 140px;
        padding: 18px 0 17px;
        font-size: 15px;
        border: 1px solid #fff;
        border-radius: 4px;
        font-weight: 700;
        color: #fff;
        text-align: center;
        margin: 0 0 0 20px;
    }
    .home_headder-wrap-sub {
        padding-right: 10px;
        padding-left: 10px;
        box-sizing: border-box;
        position: relative;
        flex: 0 0 25%;
    }
    .home-header__sub{
        position: relative;
    }
    .story__imdage-subwrap {
        display: block;
        width: 100%;
        height: auto;
        position: relative;
        overflow: hidden;
    }
    .story__imdage-subwrap::before{
        content: "";
        display: block;
        padding-bottom: 211%;
    }
    .story__image-sub {
        display: block;
        position: absolute;
        min-height: 100%;
        max-width: 100%;
        width: 100%;
        top: 0;
        bottom: 0;
        left: 0;
        right: 0;
        border-radius: 6px; 
    }
</style>