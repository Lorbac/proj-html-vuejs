<template>
    <section id="events">
        <div class="container">
            <div class="top-events">
                <h2>Upcoming Events</h2>
                <p>MEET THE AUTHOR IN PERSON</p>
            </div>
            <div class="main-events">
                <div v-for="(card, index) in cards" :key="index" class="card">
                    <img :src="require(`../${card.image}`)" alt="">
                    <h2>{{ card.title }}</h2>
                    <p>{{ card.text }}</p>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: "Events",
    data() {
        return {
            cards: [
                {
                    image: "assets/images/event-05-400x240.jpg",
                    title: "Chicago Book Signing",
                    text: "Mauris blandit aliquet elit, eget tincidunt nibh pulvinar a. Mauris blandit aliquet elit, eget tincidunt nibh pulvinar a nulla."
                },
                {
                    image: "assets/images/event-04-400x240.jpg",
                    title: "Meet & Greet With Amanda",
                    text: "Mauris blandit aliquet elit, eget tincidunt nibh pulvinar a. Praesent sapien massa, convallis a pellentesque nec, egestas."
                },
                {
                    image: "assets/images/event-07-400x240.jpg",
                    title: "Open Book: Dialogues",
                    text: "Mauris blandit aliquet elit, eget tincidunt nibh pulvinar a. Mauris blandit aliquet elit, eget tincidunt nibh pulvinar a nulla."
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>

    @import '../styles/vars.scss';

    #events {
        background-color: $dawnPink;

        .container {
            width: 80%;
            margin: 0 auto;
            display: flex;
            flex-direction: column;
            align-items: center;
            
            .top-events {
                text-align: center;

                h2 {
                    font-family: none;
                    font-size: 30px;
                    margin: 70px 0 20px 0;
                }

                p {
                    color: $saffron;
                    font-weight: 600;
                    margin-bottom: 50px;
                }
            }

            .main-events {
                display: flex;
                margin-bottom: 60px;


                .card {
                    text-align: center;
                    width: calc(100% / 3);
                    background-color: $white;
                    margin: 20px;

                    img {
                        width: 100%;
                    }

                    h2 {
                        font-weight: lighter;
                        border-bottom: 1px solid lightgray;
                        padding-bottom: 20px;
                        margin: 30px 40px;
                    }

                    p {
                        color: $scorpion;
                        line-height: 25px;
                        margin: 40px;
                    }
                }
            }
        }

    }
</style>