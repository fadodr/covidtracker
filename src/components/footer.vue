<template>
   <div>
     <div class="container">
        <div class="topcontainer">
            <div class="leftdiv">
                <div class="covid">
                   <img src="../assets/images/covidwhite.png" alt="" height="35" width="35">
                   <p>COVID-19</p>
                </div>
                <p>DesignMamba an online marketplace built to cope with promising future</p>
            </div>
            <div class="rightdiv">
                <div class="innercontainer firstcontainer">
                <p>USEFUL LINKS</p>
                <div class="linklist">
                    <div><p class="clicked">Why ?</p>
                    <p>About</p>
                    <p>Career</p>
                    <p>Blog</p>
                    <p>Contract</p></div>
                    <div>
                         <p>T&C</p>
                    <p>FAC</p>
                    <p>Privacy Policy</p>
                    </div>
                </div>
                </div>
                <div class="innercontainer secondcotainer">
                    <div>
                        <p class="locdiv">CONTACT US</p>
                        <p class="location">Tel : +2349067524305</p>
                        <p class="location">fagboola@gmail.com</p>
                    </div>
                    <div class="locdiv">
                        <p class="locdiv loc">LOCATION</p>
                        <p class="location">Lagos , Nigeria</p>
                    </div>
                </div>
                <div class="innercontainer thridcontainer">
                    <p>KEEP IN TOUCH</p>
                    <div class="circlediv">
                        <div class="circle"></div>
                        <div class="circle"></div>
                        <div class="circle"></div>
                    </div>
                </div>
            </div>
        </div>
        <div class="bottomcontainer">
            <p>© fadoinc, All Rights Reserved</p>
        </div>
    </div>
   </div>
</template>

<script>
export default {
    
}
</script>

<style scoped>
    .container {
        width: 100%;
        background-color: #262C7C;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
    }
    .bottomcontainer {
        height: 50px;
        color: white;
        font-family: 'Graphik';
        font-size: 12px;
        border-top: 1px solid #707070;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .topcontainer {
        width: 80%;
        padding: 50px 0;
        color: white;
        font-family: 'Graphik';
        font-size: 12px;
        display: flex;
        justify-content: space-between;
        margin: auto;
    }
    .covid {
        display: flex;
        align-items: center;
        padding: 15px 0;
    }
    .covid p {
        padding: 0 15px;
    }
    .leftdiv {
        width: 20%;
    }
    .rightdiv {
        width: 80%;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-around;

    }
    .innercontainer {
        width: 30%;
    }
    .linklist {
        padding: 15px 0;
        display: flex;
        justify-content: space-between;
    }
    .linklist p{
        padding-bottom: 10px;
    }
    .clicked {
        color: red;
    }
    .location{
    padding: 6px 0;}
    .locdiv {
    padding-bottom: 6px;
    }
    .loc {
    padding-top: 8px;}
    .circlediv {
        display: flex;
        padding: 8px 0;
    }
    .circle {
        height: 30px;
        width: 30px;
        border-radius: 50%;
        margin-right: 8px;
        border: 1px solid white;
    }
    @media screen and (max-width : 680px) {
        .topcontainer {
        width: 80%;
        padding: 50px 0;
        color: white;
        font-family: 'Graphik';
        font-size: 12px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        margin: auto;
    }
        .leftdiv {
        width: 100%;
        margin-bottom: 20px;
    }
    .rightdiv {
        width: 100%;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;

        }
    .innercontainer {
        width: 40%;
    }
        
    }
</style>