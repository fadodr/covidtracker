<template>
    <div class="container">
    <div class="title"><p>How coronavirus spread</p></div>
    <div class="outercon">
        <div class="innercon first">
            <img src="../assets/images/Group79.png" alt="" width="50" height="50">
            <H4>Person-to-Person spread</H4>
            <p class="content">The coronavirus is thought to spread mainly from person to person. This can happen space-between
            people who are close contact with one another</p>
        </div>
        <div class="innercon second">
         <img src="../assets/images/Group5.png" alt="" width="50" height="50">
            <H4>Person coughs or sneezes</H4>
            <p class="content">The coronavirus is thought to spread mainly from person to person. This can happen space-between
            people who are close contact with one another</p></div>
        <div class="innercon third">
         <img src="../assets/images/throat.png" alt="" width="50" height="50">
            <H4>Sore throat</H4>
            <p class="content">A sore throat can make it painful to eat and even talk. It brings scratchiness and irritation to the throat that
            can becime worse when swallowing</p></div>
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
        margin-top: 10px;
        padding: 20px 10px;
        border:  1px solid #BEC1E0;
        display: flex;
        background-color: white;
        align-items: center;
        flex-direction: column;
        border-radius: 10px;
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