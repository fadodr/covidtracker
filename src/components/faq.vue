<template>
    <div class="container">
    <div class="title"><p>FAQ</p></div>
    <div class="faqcontainer">
        <div class="leftcontainer">
            <div class="box" v-for="faq in faqs" :key="faq.name">
                <p>{{faq.name}}</p>
                <div class="triangle"></div>
            </div>
        </div>
        <div class="rightcontainer">
            <div class="rightbox" v-for="(faq, i) in faqs" :key="faq.name">
                <p>{{faq.options[i]}}</p>
                <hr />
            </div>
        </div>
    </div>
    </div>
</template>

<script>
export default {
    data(){
        return {
            faqs : [
                {
                    name : 'COVID-19',
                    options: [
                        'What is a novel coronavirus?',
                        'On February 11, 2020 the World Health Organization announced an official name for the disease that is causing the 2019 novel coronavirus outbreak',
                        'What kind of wax do you use & how long does it last?',
                        'What kind of resources do you need from me?',
                        'Does applying wax remove scratches & swirl mark'
                    ]
                },
                {
                    name : 'How it Spreads',
                    options: [
                        'What is a novel coronavirus?',
                        'On February 11, 2020 the World Health Organization announced an official name for the disease that is causing the 2019 novel coronavirus outbreak',
                        'What kind of wax do you use & how long does it last?',
                        'What kind of resources do you need from me?',
                        'Does applying wax remove scratches & swirl mark'
                    ]
                },
                {
                    name : 'How to Protect Yourself',
                    options: [
                        'What is a novel coronavirus?',
                        'On February 11, 2020 the World Health Organization announced an official name for the disease that is causing the 2019 novel coronavirus outbreak',
                        'What kind of wax do you use & how long does it last?',
                        'What kind of resources do you need from me?',
                        'Does applying wax remove scratches & swirl mark'
                    ]
                },
                {
                    name : 'Symptoms & Testing',
                    options: [
                        'What is a novel coronavirus?',
                        'On February 11, 2020 the World Health Organization announced an official name for the disease that is causing the 2019 novel coronavirus outbreak',
                        'What kind of wax do you use & how long does it last?',
                        'What kind of resources do you need from me?',
                        'Does applying wax remove scratches & swirl mark'
                    ]
                },
                {
                    name : 'Community',
                    options: [
                        'What is a novel coronavirus?',
                        'On February 11, 2020 the World Health Organization announced an official name for the disease that is causing the 2019 novel coronavirus outbreak',
                        'What kind of wax do you use & how long does it last?',
                        'What kind of resources do you need from me?',
                        'Does applying wax remove scratches & swirl mark'
                    ]
                }
            ]
        }
    }
}
</script>

<style scoped>
    .container {
        margin: auto;
        width: 100%;
        padding: 50px 0;
        border: 1px solid black;
    }
    .title {
        padding-bottom: 30px;
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .faqcontainer {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
        padding: 0 100px;
    }
    .leftcontainer {
        width: 20%;
    }
    .rightcontainer {
        width: calc(80% -200px);
        display: flex;
        flex-direction: column;
        flex-wrap: wrap;
    }
    .box {
        width: 200px;
        height: 30px;
        border: 2px solid #707070;
        border-radius: 8px;
        margin: auto;
        padding: 5px;
        margin-bottom: 10px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .box p {
    font-family: 'Graphik';
    
    color: #6468A1;}
    .rightbox {
    padding: 15px 0;}
    .rightbox p {
    padding-bottom: 10px;}
    .triangle {
        width: 0; 
        height: 0; 
        border-top: 5px solid transparent;
        border-bottom: 5px solid transparent;
        border-left: 5px solid #DADBE7;
    }
</style>