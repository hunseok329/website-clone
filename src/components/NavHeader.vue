<template>
    <header>
        <div class="hd-border">
            <div class="hd-container">
                <div class="hd-contai">
                    <div>
                        <a class="hd-logo">오늘의집</a>
                    </div>
                    <div class="hd-nav-wrapper">
                        <a class="hd-nav-wrap-a" :class="{'hd-nav-active': nav === 'community'}" v-on:click="nav = 'community', nav_sub = communitys[0]"><span>커뮤니티</span></a>
                        <a class="hd-nav-wrap-a" :class="{'hd-nav-active': nav === 'store'}" v-on:click="nav = 'store', nav_sub = stores[0]"><span>스토어</span></a>
                        <a class="hd-nav-wrap-a" :class="{'hd-nav-active': nav === 'move'}" v-on:click="nav = 'move', nav_sub = moves[0]"><span>이사/시공/수리</span></a>
                    </div>
                    <div class="hd-cont-right">
                        <div class="hd-wrapper">
                            <div class="hd-wrap-search">
                                <img class="search" src="../assets/search.png" alt="search"> 
                                <input class="search-input" type="text" placeholder="통합검색">
                            </div>
                            <a><img class="hd-wrap-cart" src="../assets/cart.png" alt="cart"></a>
                            <div class="hd-wrap-sign">
                                <a class="hd-signup">로그인</a>
                                <a class="hd-signup2">회원가입</a>
                                <!-- <a>고객센터</a> -->
                            </div>
                            <span class="hd-wrap-write">
                                <button class="write-btn">
                                    <span class="write-btn-sp">글쓰기</span>
                                </button>
                            </span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="hd-border">
            <div>
                <div class="hd-sub-container">
                    <div v-if="nav === 'community'" class="hd-sub-wrap">
                        <div v-for="item in communitys" :key="item">
                            <p class="hd-sub-wrap-p" :class="{'hd-nav-sub-active': nav_sub === item}"  v-on:click="nav_sub = item">
                                {{ item }}
                                <span v-if="betas.includes(item)" class="hd-sub-wrap-beta">BETA</span>
                            </p>
                        </div>
                    </div>
                    <div v-else-if="nav === 'store'" class="hd-sub-wrap">
                        <div v-for="item in stores" :key="item">
                            <p class="hd-sub-wrap-p" :class="{'hd-nav-sub-active': nav_sub === item}" v-on:click="nav_sub = item">
                                {{ item }}
                                <img v-if="news.includes(item)" class="nav-new-icon" src="../assets/new.png">
                            </p>
                        </div>
                    </div>
                    <div v-else class="hd-sub-wrap">
                        <div v-for="item in moves" :key="item" >
                            <p class="hd-sub-wrap-p" :class="{'hd-nav-sub-active': nav_sub === item}" v-on:click="nav_sub = item">
                                {{ item }}
                            </p>
                        </div>                
                    </div>
                    <div class="hd-sub-wrap-r">
                        <span style="color: #35C5F0; font-weight: bold;">3D인테리어</span>
                        <img src="../assets/next.png" style="height: 18px; width: 18px">
                    </div>
                </div>
            </div>
        </div>
    </header>
</template>

<script>
export default {
    name: 'NavHeader',
    data() {
        return {
            nav: "community",
            nav_sub: "홈",
            communitys: ["홈", "팔로잉", "사진", "집들이", "노하우", "전문가집들이", "셀프가이드", "질문과 답변", "3D인테리어", "이벤트"],
            stores: ["스토어홈", "카테고리", "베스트", "오늘의딜", "주방히트템", "리퍼마켓", "빠른배송", "오!굿즈", "프리미엄", "기획전"],
            moves: ["홈", "인테리어시공", "이상", "설치수리", "우리동네아파트"],
            betas: ["3D인테리어"],
            news: ["주방히트템", "리퍼마켓", "빠른배송", "프리미엄"],
        }
    },
}
</script>

<style>
    .hd-border {
        border-bottom: 1px solid #EAEDEF;
    }
    .hd-container {
        max-width: 1200px;
        margin: 0 auto;
        padding: 0 60px;
    }
    .hd-contai {
        display: flex;
        justify-content: space-between;
        height: 60px;
        padding: 10px 40px 10px 40px;
        align-items: center;
    }
    .hd-logo {
        font-size: 32px;
        margin-right: 20px;
        white-space: nowrap;
    }
    .hd-nav-wrapper {
        box-sizing: border-box;
        flex: 1 1 0px;
        white-space: nowrap;
    }
    .hd-nav-wrap-a {
        margin: 0 10px;
        padding: 21px 5px 15px;
        font-weight: bold;
    }
    .hd-nav-wrap-a:hover {
        color: #35C5F0;
    }
    .hd-nav-active {
        color: #35C5F0;
    }
    .hd-cont-right {
        flex: 0 1 476px;
    }
    .hd-wrapper {
        display: flex;
        align-items: center;
        justify-content:flex-end;
        white-space: nowrap;
    }
    .hd-wrap-search {
        display: flex;
        align-items: center;
        border: 1px solid;
        border-radius: 4px;
        padding: 0 14px;
        height: 40px;
        
    }
    .search {
        height: 24px;
        width: 24px;
    }
    .search-input {
        border: none;
    }
    .hd-wrap-cart {
        padding: 6px;
    }
    .hd-wrap-sign {
        margin: 0 10px 0 8px;
        white-space: nowrap;
    }
    .hd-signup {
        font-size: 14px;
        border-right: 1px solid;
        padding: 0 10px;
    }
    .hd-signup2 {
        display: inline;
        font-size: 14px;
        padding: 0 10px;
        white-space: nowrap;
    }
    .hd-wrap-write {
        height: 40px;
        padding: 0 12px;
        align-items: center;
        text-align: center;
        border-radius: 4px;
        background-color: #35C5F0;
    }
    .write-btn {
        border: 0;
        outline: 0;
        height: 40px;
        background-color: #35C5F0;
        color: #FFFFFF;
    }
    .write-btn-sp {
        font-size: 14px;
        white-space: nowrap;
    }
    .hd-sub-container {
        max-width: 1136px;
        margin: 0 auto;
        padding: 0 60px;
        display: flex;
        align-items: center;
    }
    .hd-sub-wrap {
        display: flex;
        padding: 0;
        box-sizing: border-box;
        flex: 1 0 0px;
    }
    .hd-sub-wrap-r {
        display: flex;
        align-items: center;
    }
    .hd-sub-wrap-p {
        margin: 0 5px;
        padding: 12px 6px;
        white-space: nowrap;
        display: flex;
        align-items: center;
        font-weight: bold;
    }
    .hd-sub-wrap-p:hover {
        color: #35C5F0;
    }
    .hd-nav-sub-active {
        color: #35C5F0;
        border-bottom: 2px solid #35C5F0;
    }
    .hd-sub-wrap-beta {
        display: inline-block;
        color: rgb(255, 255, 255);
        background-color: rgb(130, 140, 148);
        padding: 0 4px;
        font-size: 10px;
        height: 16px;
        border-radius: 4px;
        line-height: 16px;
    }
    .nav-new-icon {
        height: 18px;
        width: 18px;
    }
</style>