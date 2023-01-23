<template >
    <div class="main">
        <div class="wrapper">
            <input type="checkbox" id="check-menu">
            <label for="check-menu"></label>
            <div class="burger-line first"></div>
            <div class="burger-line second"></div>
            <div class="burger-line third"></div>
            <div class="burger-line fourth"></div>
            <nav class="main-menu">
                <a href="#">Contact</a>
                <a href="#">About</a>
                <a href="#">Work</a>
            </nav>
        </div>
        <div class="menu">
            <div class="bell">
                <img src="./icon/Re25.png" alt="bells">
            </div>
            <div class="vector">
                <img src="./icon/Vector.png" alt="vect">
            </div>
        </div>
        <div class="search">
            
            <input class="input" type="text" placeholder="Search">
        </div>
        <div class="tabs">
            <span>Current Balance</span>
            <img class="dotfirst" src="./icon/dot.png" alt="dot"> 
            <button class="btn">Quick Invest</button>
            <button class="btn">Show Report</button>
         </div>
         <div class="tab">
            <img class="dotsecond" src="./icon/dot.png" alt="dot">
            <span>Summary</span>
        </div>
        <div class="tabfinal">
            <span class="tabwords">Summary</span>
            <span class="tabwords1">Table</span>
            <span class="tabwords2">Charts</span>
            <span class="tabwords3">Reporting</span>
            <span class="tabwords4">Analysis</span>
            <button class="btn_tabs">Sell</button>
            <button class="btn_tabs">Buy</button>
            <button class="btn_tabs">Sell</button>
            <button class="btn_tabs">Buy</button>
            <button class="btn_tabs">Sell</button>
            <button class="btn_tabs">Buy</button>
        </div>
        <div class="sidenav">
            <div class="logo">
                <img class="payte" src="./icon/Payte.png" alt="payte">
            </div>
            <div class="circle1">
                <img src="./icon/cirle1.png" alt="circle1">
            </div>
            <div class="circle2">
                <img src="./icon/cirle2.png" alt="circle2">
            </div>
             
                <a class="over" href="#">Overview</a>
                <a class="buy" href="#">Buy / Sell</a>
                <a class="wall" href="#">Wallets</a>
                <a class="bund" href="#">Bundles</a>
                <a class="rep" href="#">Reporting</a>
                <a class="com" href="#">Community</a>
            <div class="fav">
                <span class="fav">Favorites</span>
                <img class="dot" src="./icon/dot.png" alt="dot">
            </div>
            <div class="crypto">
                <div class="btc">
                    <span class="btc-first">BTC</span>
                    <span class="btc-second">Bitcoin</span>
                    <img class="btcicon" src="./icon/VectorBtc.png" alt="btcpng">
                    <img class="btcicon1" src="./icon/Group27.png" alt="btcicon1">
                </div>
                <div class="ripple">
                    <span class="rpl-first">XRP</span>
                    <span class="rpl-second">Ripple</span>
                    <img class="rpicon1" src="./icon/VectorRpl.png" alt="rplpng">
                    <img class="rplicon" src="./icon/Group28.png" alt="rplicon"> 

                </div>
            </div>
        </div>
    </div>
    
    
</template>
<script>
import axios from 'axios'; 

export default {
    data() {
        return
    },
methods: {

    async fetchInform() {
        try{
            const response = await axios.get('https://sandbox-api.coinmarketcap.com/v1/cryptocurrency/listings/latest', {
                headers: {
                    'X-CMC_PRO_API_KEY': '2efd0eac-7c80-4a2e-892a-899bf6f6cefd',
        },
        })
        console.log(response); //
        } catch(e) {
            alert('Error')
        }
    }
}    
}

</script>


<style>

    @font-face {
        font-family: 'SF Pro Display';
        src: url("../sheets/SFPRODISPLAYREGULAR.OTF");
    }

    .btc-first {
        margin-left: 68px;
        width: 22px;
        height: 14px;
        color: #9896A1;
        font-family: 'SF Pro Display';
        font-style: normal;
        font-weight: 400;
        font-size: 12px;
        line-height: 14px;
    }

    .btc-second {
        margin-left: 68px;
        top: 785px;
        font-family: 'SF Pro Display';
        font-style: normal;
        font-weight: 600;
        font-size: 12px;
    }

    .rpl-first {
        margin-left: 68px;
        width: 22px;
        height: 14px;
        color: #9896A1;
        font-family: 'SF Pro Display';
        font-style: normal;
        font-weight: 400;
        font-size: 12px;
        line-height: 14px;
    }

    .rpl-second {
        margin-left: 68px;
        top: 850px;
        font-family: 'SF Pro Display';
        font-style: normal;
        font-weight: 600;
        font-size: 12px;
    }

    * { 
        font-family: 'SF Pro Display';
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }
    
    .payte {
        margin-top: 40px;
        margin-left: 66px;
    }

    .circle1 {
        margin-left: 10px;
        margin-top: -30px;
    }
    .circle2 {
        margin-left: 20px;
        margin-top: -30px;
    }

    .main {
        max-width: 1440px;
        max-height: 900px;
        
        
    }

    .fav {
        margin-left: 10px;
        font-family: 'SF Pro Display';
        font-size: 14px;
        color: #9896A1;
        top: 720px;

    }

    .dot {
        margin-left: 210px;
        position: absolute;
    }

    .sidenav {
        width: 264px;
        height: 900px;
        background: #F7F7F9;
        position: fixed;
        top: 0;
        left: 0;
    
    }

    .sidenav a {
        display: block;
        text-decoration: none;
        font-size: 16px;
        color: #0A041C;
        padding: 30px 32px;
        margin: 32px 60px ;
        border-radius: 4px;
        opacity: 40%;
    }
    .over {
        background-image: url('./icon/Icon1.png');
        background-repeat: no-repeat;
        background-position: left;
    }
    .buy {
        background-image: url('./icon/Icon.png');
        background-repeat: no-repeat;
        background-position: left;

    }
    .wall {
        background-image: url('./icon/Icon3.png');
        background-repeat: no-repeat;
        background-position: left;
    }

    .bund {
        background-image: url('./icon/Icon4.png');
        background-repeat: no-repeat;
        background-position: left;
    }

    .rep {
        background-image: url('./icon/Icon5.png');
        background-repeat: no-repeat;
        background-position: left;
    }

    .com {
        background-image: url('./icon/Icon6.png');
        background-repeat: no-repeat;
        background-position: left;
    }
    

    .sidenav a:hover {
        background: #FFFFFF;
        color: #0A041C;
        
        
    }

    .tabs {
        
        width: 509px;
        height: 336px;
        margin-left: 320px;
        margin-top: 129px;
        background-color: #F7F7F9;
        border-radius: 16px;
    }
    .tab {
        width: 499px;
        height: 336px;
        margin-left: 880px;
        margin-top: -335px;
        background-color: #F7F7F9;
        border-radius: 16px;
    }

    .input {
        background-image: url('./icon/Icon8.png');
        position: absolute;
        width: 232px;
        height: 48px;
        left: 320px;
        top: 49px;
        background: #F7F7F9;
        border-radius: 8px;
        font-family: 'SF Pro Display';
        font-size: 14px;
        color: #9896A1;
        text-align: center;
        border: none;
        outline: none;
    }

    .bell {
        margin-top: 49px;
        margin-left: 1260px;
        cursor: pointer;
    }

    .vector {
        margin-left: 1275px;
        margin-top: -35px;
        
    }

    .wrapper {
        position: absolute;
        margin-left: 1315px;
        width: 48px;
        height: 48px;
        background-color: #F7F7F9;
        color: white;
        text-align: center;
        border-radius: 8px;
        font-family: 'SF Pro Display';
     
    }
    #check-menu {
        display: none;
    }

    label {
        display: block;
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        cursor: pointer;
        z-index: 2;
    }

    .burger-line {
        position: absolute;
        width: 12.34px;
        height: 0px;
        left: 0.83px;
        top: 1.72px;
        background-color: #9896A1;
        border: 2px solid #9896A1;

    }

    .second, .third {
        top: 19px;
        left: 18px;
    }

    .fourth {
        top: 28px;
        left: 18px;
    }

    .first {
        top: 10px;
        left: 18px;
    }

    .main-menu {
        position: absolute;
        display: block;
        width: 320px;
        bottom: 0;
        left: 0;
        transform: translateY(100%);
        max-height: 0;
        font-size: 0;
        overflow: hidden;
    }

    a {
        display: block;
        width: 100%;
        padding: 10px;
        color:#0A041C;
        text-decoration: none;
        border-top: 1px solid rgba(rgb(190, 189, 189), rgb(138, 138, 138), rgb(119, 119, 119),.3);
        background-color: #F7F7F9;
    }

    #check-menu:checked ~.main-menu {
        max-height: 500px;
        font-size: 16px;

    }

    span {
        position: absolute;
        font-family: 'SF Pro Display';
        font-style: normal;
        font-weight: 500;
        font-size: 20px;
        line-height: 24px;
        margin-left: 32px;
        margin-top: 32px;
    }

    .btn {
        box-sizing: border-box;
        font-family: 'SF Pro Display';
        font-style: normal;
        width: 112px;
        height: 40px;
        background: #FFFFFF;
        border: 1px solid #EBEBF3;
        border-radius: 4px;
        margin-left: 32px;
        margin-top: 264px;
        

    }
    .btn:hover {
        background: #7445FB;
        border-radius: 4px;
    }

    .btcicon {
        margin-left: 170px;
        margin-top: 32px;
    }

    .btcicon1 {
        position: absolute;
        margin-top: 45px;
        left: 24px;
    }

    .rplicon {
        position: absolute;
        margin-top: 30px;
        left: 16px;
    }

    .rpicon1 {
        margin-left: 170px;
        margin-top: 32px;
    }

    .tabfinal {
        display: flex;
        position: absolute;
        width: 1060px;
        height: 300px;
        left: 320px;
        top: 590px;
        background: #F7F7F9;
        
        
    }

    .tabwords {
        font-family: 'SF Pro Display';
        font-style: normal;
        font-weight: 400;
        font-size: 16px;
        color: #9896A1;
        
    }

    .tabwords1 {
        margin-left: 110px;
        font-family: 'SF Pro Display';
        font-style: normal;
        font-weight: 400;
        font-size: 16px;
        color: #9896A1;
    }

    .tabwords2 {
        margin-left: 165px;
        font-family: 'SF Pro Display';
        font-style: normal;
        font-weight: 400;
        font-size: 16px;
        color: #9896A1;
    }

    .tabwords3 {
        margin-left: 230px;
        font-family: 'SF Pro Display';
        font-style: normal;
        font-weight: 400;
        font-size: 16px;
        color: #9896A1;
    }

    .tabwords4 {
        margin-left: 320px;
        font-family: 'SF Pro Display';
        font-style: normal;
        font-weight: 400;
        font-size: 16px;
        color: #9896A1;
    }

    .tabwords:hover {
        font-family: 'SF Pro Display';
        font-style: normal;
        font-weight: 500;
        font-size: 16px;
        line-height: 24px;
        text-decoration: underline;
        color: #0A041C;
    }

    .dotfirst {
        position: absolute;
        left: 770px;
        top:250px;
        
    }
    .dotsecond {
        position: absolute;
        left: 1320px;
        top:250px;
    }

    .btn_tabs {
        background: #FFFFFF;
        border: 1px solid #EBEBF3;
        border-radius: 4px;
        box-sizing: border-box;
        width: 55px;
        height: 40px;
        justify-content: space-between;
        align-items: flex-end;
        margin-top: 270px;
        margin-right: 20px;

        
    }

    .btn_tabs:hover {
        background: #7445FB;
        border-radius: 4px;
        color: #FFFFFF;
    }




    @media screen and (max-width: 1440px) {
	.container {
		width: 1200px;
	}
}
    
    
</style>