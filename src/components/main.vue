<template>
    <div class="mainpage">
        <div class="firstdiv">
        <h3>COVID-19 LIVE TRACKER</h3>
        <p>The coronavirus (COVID-19) was first reported in Wuhan, Hubei, China in December 2019, the outbreak
        was later recpgnized as a pandemic by the World Health Organization (WHO) on 11 March 2020</p>
        <div class="buttons">
            <button id="firstbutt">How to Protect</button>
            <button id="secondbutt">FIND A DOCTOR</button>
        </div>
        </div>
        <div class="seconddiv">
            <img src="../assets/images/emo.png" alt="">
        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style scoped>
.mainpage {
    width: 100%;
    padding: 50px 0;
    display: flex;
    justify-content: center;
    background-color: #262C7C;
    align-items: center;
}
.firstdiv {
    width: 50%;
    padding: 0 10%;
    background-color: #262C7C
}
.firstdiv p {
     font-family: "Graphik";
    color: white;
    font-size: 12px;
    background-color: #262C7C;
    margin-bottom: 20px;
}
.seconddiv {
    width: 50%;
    padding: 0 10%;
    background-color: #262C7C
}
.buttons button{
    margin: 10px;
    padding: 10px 15px;
    outline: none;
    border-radius: 8px;
}
h3 {
    font-family: "Graphik";
    color: white;
    background-color: #262C7C;
    padding: 20px 0;
}
#firstbutt {
    background-color: #EB0065;
    border-color: #EB0065;
    color: white;
    margin-right: 25px;
    font-family: "Graphik";
}
#secondbutt {
    background-color: #262C7C;
    border-color: white;
    margin-bottom: 20px;
    color: white;
}
img{
        max-width: 100%;
        max-height: 100%;
        display: block; /* remove extra space below image */
    }
@media screen and (max-width : 760px) {
    .mainpage {
        flex-wrap: wrap;
    }
    .firstdiv {
        width: 100%;
    }
    .seconddiv {
        width: 50%;
    }
}
</style>