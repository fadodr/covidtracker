<template>
    <div class="container">
    <div class="title"><p>Blog Topics</p></div>
    <div class="outercon">
        <div class="innercon first">
            <div class="topcontainer"></div>
            <div class="bottomcontainer">
                <h4>wearing face mask working</h4>
                <p class="content">If you wear a mask, then you must know how to use it and dispose of it properly. When…</p>
                <div class="datediv">
                    <p class="date">10 MAR 2020</p>
                    <p class="read">read more</p>
                </div>
            </div>
        </div>
        <div class="innercon second">
        <div class="topcontainer"></div>
            <div class="bottomcontainer">
                <h4>Cleaning hands with sanitizer</h4>
                <p class="content">Washing your hands can protect you and your ... Also, alcohol-based hand sanitizer kills the coronavirus…</p>
                <div class="datediv">
                    <p class="date">10 MAR 2020</p>
                    <p class="read">read more</p>
                </div>
            </div></div>
        <div class="innercon third">
        <div class="topcontainer"></div>
            <div class="bottomcontainer">
                <h4>Stay home</h4>
                <p class="content">Stay home. Save lives As COVID-19 continues to impact communities around the world…</p>
                <div class="datediv">
                    <p class="date">10 MAR 2020</p>
                    <p class="read">read more</p>
                </div>
            </div></div>
    </div>
    <div class="butt"><button>View All</button></div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style scoped>
    .container {
        margin: auto;
        width: 70%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        padding: 50px 0;
    }
    .title {
        padding-bottom: 30px;
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        font-family: 'Graphik';
        color: #6468A1;
    }
    .outercon {
        width: 100%;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
    }
    .innercon {
        width: 25%;
        padding-bottom: 30px;
        border-radius: 10px;
    }
    .topcontainer {
        height: 100px;
        border-top-left-radius: 10px;
        border-top-right-radius: 10px;
        background-color: #C6C6C6;
    }
    .datediv {
        display: flex;
        justify-content: space-between;
    }
    h4 {
        font-family: 'Graphik';
        color: #6468A1;
    }
    .content {
        font-family: 'Graphik';
        font-size: 12px;
        padding: 18px 0;
        color: #6468A1;
    }
    .bottomcontainer{
        padding: 20px 10px;
        background-color: white;
        text-align: justify;
        border-bottom-left-radius: 10px;
        border-bottom-right-radius: 10px;
    }
    .date {
        font-family: 'Graphik';
        font-size: 8px;
        color:  #878AA1;
       
    }
     .read {
        font-family: 'Graphik';
        font-size: 10px;
        color:  #6468A1;
       
    }
    button {
        background-color: #EB0065;
        color: white;
        padding: 7px 20px;
        outline: none;
        border: none;
        border-radius: 5px;
        font-family: 'Graphik';
        font-size: 12px;
    }
    @media screen and (max-width : 770px) {
        .innercon {
            width: 40%;
        }
    }
    @media screen and (max-width : 460px) {
        .innercon {
            width: 80%;
        }
        .outercon {
            display: flex;
            justify-content: center;
        }
    }
</style>