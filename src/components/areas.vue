<template>
    <div class="container">
        <div class="leftdiv">
            <div class="topleftdiv">
                <p>Covid-19 Affected Areas</p>
                <div class="affected">
                    <div class="affectedicon">
                        <p>Most Affected</p>
                        <img src="../assets/images/redicon.png" alt="">
                    </div>
                    <div class="affectedicon">
                        <P>Less Affected</P>
                        <img src="../assets/images/greenicon.png" alt="">
                    </div>
                </div>
            </div>
        </div>
        <div class="rightdiv">
            <input type="text" placeholder="Filter to a location">
            <div class="global">
                <p>Global</p>
                <p>{{global}}</p>
            </div>
            <hr>
             <div class="globalloop" v-for="w in world" :key="w.Country">
                <div class="countryimg">
                    <img :src="w.flag" alt="">
                    <p>{{w.Country}}</p>
                </div>
                <p class="countries">{{w.TotalConfirmed}}</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    created(){
    this.axios.get('https://api.covid19api.com/summary').then((response) => {
        let allcountries = []
        let searchcountries = ['United States of America', 'Spain', 'Italy', 'Germany', 'China', 'France', 'Iran, Islamic Republic of', 'United Kingdom']
        let flag = [require('../assets/images/usa.png'),require('../assets/images/spain.png'), require('../assets/images/italy.png'),
        require('../assets/images/germany.png'),require('../assets/images/china.png'),require('../assets/images/france.png'),require('../assets/images/iran.png'),
        require('../assets/images/uk.png')]
        this.global = response.data.Global.TotalConfirmed
        for(let i = 0; i < searchcountries.length; i++){
            allcountries.push(response.data.Countries.find(x =>
            x.Country == searchcountries[i]
        ))
        }
        let j=0
        allcountries.forEach(x => {
            this.world.push({
                Country : x.Country,
                TotalConfirmed : x.TotalConfirmed,
                flag : flag[j++]
            })
        })
    }).catch((error) => console.log(error))
     },
    data(){
        return {
            global : '',
            world : [],
        }
    }
}
</script>

<style scoped>
    .container {
        margin: auto;
        width: 70%;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
    }
    .leftdiv {
        margin: 0 auto;
        width: 60%;
            border: 1px solid black;
        padding: 10px 15px;
        margin-top: 30px;
        height: 200px;
    }
    .topleftdiv {
        display: flex;
        justify-content: space-between;
    }
    .affected {
        display: flex;
        justify-content: space-between;
    }
    .rightdiv {
        margin: 0 auto;
        margin-top: 30px;
            border: 1px solid black;
            padding: 10px 30px;
            background-color: white;
    }
    .affectedicon {
        padding-left: 30px;
    }
    .affectedicon p {
    display: inline;}
    .affectedicon img {
        padding-left: 10px;
    }
    .global {
        display: flex;
        justify-content: space-between;
        border: 1px solid #262C7C;
        padding: 10px;
        border-radius: 5px;
    }
    .countryimg {
    display: flex;
    align-items: center;
    margin-right: 5px;}
    .countryimg p {
    margin-left: 8px;}
    .global p {
    color: #6468A1;}
    .globalloop {
        display: flex;
        align-items: center;
        justify-content: space-between;
        border: 1px solid transparent;
        border-radius: 5px;
        padding: 10px;
        margin-bottom: 10px;
        background-color: #F2F3F7;
    }
    input {
        width: calc(100% - 20px);
        margin: 10px 0;
        padding: 10px;
        border: 1px solid #B8BACC;
        border-radius: 5px;
    }
    hr {
    margin: 15px 0;}
    .countries {
    color: #6468A1;}
    @media screen and (max-width : 1122px) {
        .leftdiv {
            width: 100%;
        }
    }
</style>