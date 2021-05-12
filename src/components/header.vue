<template>
    <div>
        <div class="navbar">
        <div class="title">
            <img src="../assets/images/covidwhite.png" alt="" height="35" width="35">
            <p>Covid-19</p>
        </div>
        <div class="navitems"> 
            <p>Home</p>
            <p>Our Results</p>
            <p>Exterior</p>
            <p>Interior</p>
            <p>About Us</p>
            <p>Contact Us</p>
        </div>
        <button @click="togglebutton">
            <div class="btn btnicontop" :class="{'isactivetop' : isShow}"></div>
            <div class="btn btniconmiddle" :class="{'isactivemiddle' : isShow}"></div>
            <div class="btn btnicondown" :class="{'isactivebottom' : isShow}"></div>
        </button>
    </div>
    <ul class="list" :class="{'showlist' : isShow}">
        <li>Home</li>
        <li>Our Results</li>
        <li>Exterior</li>
        <li>Interior</li>
        <li>About Us</li>
        <li>Contact Us</li>
    </ul>
    </div>
</template>

<script>
export default {
    data() {
        return {
            isShow : false,
        }
    },
    methods : {
        togglebutton(){
            this.isShow = !this.isShow
            this.$emit('togglebutton')
        }
    }
}
</script>

<style scoped>
    .navbar{
        height: 50px;
        display: flex;
        justify-content: space-between;
        background-color: #262C7C;
        align-items: center;
        padding: 0 10%;
        border-bottom: 1px solid #707070;
    }
    .navitems{  
        display: flex;
    }
    .title {
        display: flex;
        align-items: center;
    }
    .title p {
    margin-left: 5px;}
    .navitems p {
        padding: 0 20px;
    }
    p {
        color: white;
    }
    button {
        border: none;
        background: none;
    }
    .btn {
        height: 2px;
        width: 20px;
        background-color: white;
        transition: all 0.5s;
        margin: 3px 0;
    }
    .isactivetop {
        transform:translate(-5px, 5px) rotate(45deg);
    }
    .isactivemiddle {
        background: transparent;
    }
    .isactivebottom {
        transform:translate(-5px, -5px) rotate(-45deg);
    }
    button:active, button:focus {
        outline: none;
    }
    .list {
        display: none;
    }
    @media screen and (max-width : 880px){
        .navitems {
            display: none;
        }
        .showlist{
            display: block;
            height: calc(100vh - 50px);
            width: 100%;
            background-color: #262C7C;
            color: white;
            text-align: center;
        }
        .showlist li {
            padding: 15px 0;
            font-size: 20px;
        }
    }
    @media screen and (min-width : 880px) {
        button {
            display: none;
        }
        
    }
</style>