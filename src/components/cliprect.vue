<template>
    <div class="container">
        <div class="divs firstdiv">
            <img src="../assets/images/globe.png" alt="" height="40" width="40">
            <div class="globediv">
                <p>Stats Overview</p>
                <div class="globearrow">
                    <p>Global</p>
                    <p><em class="arrow down"></em></p>
                </div>
            </div>
            <div class="innercontainer">
            <div class="redcircle"></div>
                <p class="live">Live</p>
            </div>
        </div>
        <div class="divs seconddiv">
            <img src="../assets/images/covidorange.png" alt="" height="40" width="40">
            <div class="globediv">
                <p>Total Coronavirus Cases</p>
                <p>{{totalCases}}</p>
            </div>
        </div>
        <div class="divs thirddiv">
             <img src="../assets/images/covidgreen.png" alt="" height="40" width="40">
            <div class="globediv">
                <p>Total Recovered</p>
                <p>{{totalRecovered}}</p>
            </div>
        </div>
        <div class="divs fourthdiv">
             <img src="../assets/images/covid1.png" alt="" height="40" width="40">
            <div class="globediv">
                <p>Total Deaths</p>
                <p>{{totalDeath}}</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data(){
        return {
            totalCases : '',
            totalRecovered : '',
            totalDeath : ''
        }
    },
    mounted(){
    this.axios.get('https://api.covid19api.com/summary').then((response) => {
        this.totalCases = response['data']['Global']['TotalConfirmed']
        this.totalDeath = response['data']['Global']['TotalDeaths']
        this.totalRecovered = response['data']['Global']['TotalRecovered']
    }).catch((error) => console.log(error))
  }
}
</script>

<style scoped>
    .container {
        margin: auto;
        margin-top: -50px;
        width: 70%;
        border: 5px solid transparent;
        display: flex;
       justify-content: center;
       z-index: 3;
       background-color: white;
       border-radius: 10px;
       padding: 15px 0;
    }
    .divs {
        width: 22%;
        margin: auto;
        padding: 7px 0;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-evenly;
    }
    .arrow {
  border: solid black;
  border-width: 0 3px 3px 0;
  display: inline-block;
  padding: 3px;
}
.down {
  transform: rotate(45deg);
  -webkit-transform: rotate(45deg);
}
.globearrow {
    display: flex;
    justify-content: space-between;
}
.redcircle {
width: 7px;
height: 7px;
border-radius: 50%;
background-color: #FF3E29;}
.innercontainer {
display: flex;
justify-content: space-between;
padding: 0 5px;
align-items: center;
background-color: #FFEDEB;
height: max-content;
border: 1px solid transparent;
}
.live {
color: #FF3E29;}
.globediv {
display: flex;
flex-direction: column;
justify-content: space-between;}
</style>