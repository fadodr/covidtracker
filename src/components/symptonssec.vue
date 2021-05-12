<template>
    <div class="container">
    <div class="title"><p>Symptons of CoronaVirus</p></div>
    <div class="outercon">
        <div class="innercon first">
            <img src="../assets/images/Group230.png" alt="" width="50" height="50">
            <H4>Wash your hands regularly with soap</H4>
            <p class="content">Handwashing is one of the best ways to protect yourself and your family from 
            getting sick. Learn when and how you should wash your hands to stay healthy</p>
        </div>
        <div class="innercon second">
         <img src="../assets/images/Group7.png" alt="" width="50" height="50">
            <H4>Stay home if you feel unwell.</H4>
            <p class="content">Most people with COVID-19 have mild illness and are able to recover at home without medical care. 
            Do not leave your home, except to get medical care. </p></div>
        <div class="innercon third">
         <img src="../assets/images/Group4.png" alt="" width="50" height="50">
            <H4>Avoid touching your face.</H4>
            <p class="content">To help prevent infections, keep your hands away from your eyes, 
            nose, and mouth. Why? Touching the mucous membranes on your face.</p></div>
        <div class="innercon fourth">
         <img src="../assets/images/Group5.png" alt="" width="50" height="50">
            <H4>Cover your mouth and nose</H4>
            <p class="content">Cover your mouth and nose with a tissue when you cough or sneeze. 
            Put your used tissue in a waste basket. If you don't have a tissue, cough or sneeze into your.</p></div>
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
        justify-content: center;
        font-family: 'Graphik';
        color: #6468A1;
        align-items: center;
    }
    .outercon {
        width: 100%;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-around;
    }
    .innercon {
        width: 20%;
        padding: 30px 0;
        text-align: justify;
    }
    H4 {
        padding: 15px 0;
        font-family: 'Graphik';
        color: #6468A1;
    }
    .content {
         font-family: 'Graphik';
        font-size: 12px;
        color: #6468A1;
    }
    @media screen and (max-width : 740px) {
        .innercon {
            width: 45%;
        }
    }
</style>