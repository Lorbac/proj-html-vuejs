<template>
    <section id="more-about-author">
        <div class="title">
            <h2>Dig a Little Deeper Into Damon Vaughn</h2>
            <p>FIND OUT MORE ABOUT THE AUTHOR HIMSELF</p>    
        </div>
        <div class="cards">
            <div class="card" :style="{ backgroundImage: 'linear-gradient(rgba(0, 0, 0, 0.1) 0%, rgba(0, 0, 0, 0.9) 100%), url(' + require(`../${card.bgImages}`) + ')'}" v-for="(card, index) in cards" :key="index">
                <h4>{{card.name}}</h4>
                <p>{{card.subtitle}}</p>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: "MoreAboutTheAuthor",
    data() {
        return {
            cards: [
                {
                    name: "About Me",
                    subtitle: "Vestibulum andte ipsum primis",
                    bgImages: "assets/images/box-1.jpg"
                },
                {
                    name: "My Latest Book",
                    subtitle: "Vestibulum andte ipsum primis",
                    bgImages: "assets/images/box-3.jpg"
                }
                ,
                {
                    name: "Book Signing",
                    subtitle: "Vestibulum andte ipsum primis",
                    bgImages: "assets/images/box-4.jpg"
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>

    @import '../styles/vars.scss';

    #more-about-author {

        .title {
            text-align: center;
            h2 {
                font-family: none;
                font-size: 40px;
                margin: 40px 0;
            }

            p {
                color: $keppel;
                margin: 20px;
                letter-spacing: 3px;
            }
        }

        .cards {
            width: 75%;
            display: flex;
            justify-content: center;
            text-align: center;
            margin: 0 auto;

            .card {
                flex-basis: calc(100% / 3);
                margin: 30px;
                border-radius: 0 0 90px;
                background-repeat: no-repeat;
                background-size: cover;
                
                h4 {
                    color: $white;
                    padding: 20px;
                    position: relative;
                    font-size: 30px;
                    margin-top: 350px;
                    

                    &::after {
                        content: "";
                        background-color: gray;
                        position: absolute;
                        height: 2px;
                        bottom: 0;
                        left: 40%;
                        width: 20%;
                    }
                }

                p {
                    color: $saffron;
                    margin: 40px 0;
                }
            }
        }
    }
</style>