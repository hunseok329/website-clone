<template>
    <header>
        <div class="">
            <div class="hd-container">
                <div>
                    <a class="hd-logo">오늘의집</a>
                </div>
                <div class="hd-nav-wrapper">
                    <a class="hd-nav-wrap-a"><span>커뮤니티</span></a>
                    <a class="hd-nav-wrap-a"><span>스토어</span></a>
                    <a class="hd-nav-wrap-a"><span>이사/시공/수리</span></a>
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
    </header>
</template>

<script>
export default {
    name: 'NavHeader',
}
</script>

<style>
    .hd-container {
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
</style>