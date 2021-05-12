<template>
    <div class="container">
    <div class="title"><p>Symptons of CoronaVirus</p></div>
    <div class="outercon">
        <div class="innercon first">
         <img src="../assets/images/Fever.png" alt="" width="50" height="50">
            <H4>Fever</H4>
            <p class="content">High Fevr - this means you feel hot to touch on your chest or backk ( you do not need to measure your temperature). 
            It is  a common sign and also may appear in 2-10 days if you are affected</p></div>
        <div class="innercon second">
         <img src="../assets/images/throat.png" alt="" width="50" height="50">
            <H4>Dry cough</H4>
            <p class="content">Continuous cough - this means coughing a lot for more than an hour, or 3 or more coughing episode in 24hours
             (if you usually have a cough, it may be worse than usual)</p></div>
        <div class="innercon third">
         <img src="../assets/images/sore.png" alt="" width="50" height="50">
            <H4>Sore Throat</H4>
            <p class="content">A sore throat can make it painful to eat and evn talk. It brings scratchiness and irritation to the 
            throat that can become worse when swallowing</p></div>
    </div>
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
        padding: 50px 0;
    }
    .title {
        padding-bottom: 30px;
        width: 100%;
        display: flex;
        font-family: 'Graphik';
        color: #262C7C;
        justify-content: center;
        align-items: center;
    }
    .outercon {
        width: 100%;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
    }
    .innercon {
        width: 25%;
        padding: 20px 10px;
        border:  1px solid #BEC1E0;
        display: flex;
        background-color: white;
        align-items: center;
        flex-direction: column;
        border-radius: 10px;
        margin-top: 10px;
        box-shadow: 0 4px 8px 0 #BEC1E0;
        transition: 0.3s;
    }
    H4 {
        font-family: 'Graphik';
        color: #262C7C;
        background-color: white;
        padding-top: 10px;
    }
    .content {
        text-align: center;
        background-color: white;
        font-family: 'Graphik';
        font-size: 12px;
        color: #6468A1;
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