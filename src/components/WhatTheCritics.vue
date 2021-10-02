<template>
  <section id="what-the-critics">
        <div class="top-section">
            <div class="text-left-side">
                <h2>What The Critics Say</h2>
                <p>TESTIMONIALS FROM AROUND THE WORLD</p>
            </div>
            <div class="button-right-side">
                Read All Testimonials
            </div>
        </div>
        <div class="bottom-section">
            <div class="left-side-articles">
                <h2>Best Author Of His Generation</h2>
                <h4>This book will change your perspective on life</h4>
                <p>
                    Donec fringilla nunc eu turpis dignissim, at euismod sapien tincidunt. Maecenas eleifend congue cursus. In vitae enim quis sem pharetra.Curabitur arcu erat, accumsan id imperdiet et, porttitor at sem. 
                </p>
                <p>
                    Donec fringilla nunc eu turpis dignissim, at euismod sapien tincidunt. Maecenas eleifend congue cursus. In vitae enim quis sem pharetra.Curabitur arcu erat, accumsan id imperdiet et, porttitor at sem. Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio error totam nostrum saepe sequi facere magni vel non.
                </p>
                <div class="nytimes">
                    <img src="../assets/images/nytimes-logo-white-xsmall.png" alt="New York Times logo">
                    <span>Justine Kilpatrick, </span><span>The New York Times</span>
                </div>
            </div>
            <div class="right-side-articles">
                <div class="top-right-side-article">
                    <h3>
                        A True Masterpiece, Bravo!
                    </h3>
                    <p>
                        Nulla quis lorem ut libero malesuada feugiat. Vivamus magna justo, lacinia eget consectetur sed, convallis at tellus. Vivamus suscipit tortor eget felis porttitor volutpat. Nulla quis lorem ut libero malesuada feug at.
                    </p>
                </div>
                <div class="theGuardian">
                    <img src="../assets/images/theguardian-xsmall.png" alt="The Guardian logo">
                    <span>Gerald Hendley, </span><span>The Guardian</span>
                </div>
                <div class="bottom-right-side-article">
                    <h3>
                        A Unique View On The World
                    </h3>
                    <p>
                        Donec sollicitudin molestie malesuada. Curabitur arcu erat, accumsan id imperdiet et, porttitor at sem. Vestibulum ac diam sit amet quam vehicula elementum sed sit amet dui. Nulla quis lorem ut libero malesuada feugiat. Vestibulum ac diam sit amet.
                    </p>
                </div>
                <div class="theGlobeAndMail">
                    <img src="../assets/images/globe-xsmall.png" alt="The Globe And Email logo">
                    <span>Mary Maxey, </span><span>The Globe And Mail</span>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: "WhatTheCritics"
}
</script>

<style lang="scss" scoped>

    @import '../styles/vars.scss';

    #what-the-critics {
        
        .top-section {
            margin: 0 auto;
            width: 70%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: 100px;
            margin-bottom: 60px;

            .text-left-side {

                h2 {
                    font-family: none;
                    font-size: 45px;
                    margin: 0 0 30px 0;
                }

                p {
                    color: $blueLagoon;
                    font-weight: 600;
                    letter-spacing: 2px;
                }
            }

            .button-right-side {
                background-color: $anzac;
                color: $white;
                padding: 15px 50px;
                border-radius: 5px;
                cursor: pointer;
                transition: 0.1s ease-out;

                &:hover {
                    transition: 0.1s linear;
                    background-color: $cornHarvest;
                }
            }
        }

        .bottom-section {
            display: flex;
            width: 70%;
            margin: 10px auto;
            margin-bottom: 100px;

            .left-side-articles {
                background-image: linear-gradient(rgba(0, 0, 0, 0.1) 0%, rgba(22, 22, 22, 0.7) 100%), url("../assets/images/testimonial2-2x.jpg");
                background-repeat: no-repeat;
                background-size: cover;
                border-radius: 0 0 90px;
                color: $white;
                display: flex;
                flex-direction: column;
                justify-content: center;
                padding: 0 80px;

                h2 {
                    font-family: none;
                    font-size: 42px;
                    border-bottom: 1px solid $scorpion;
                    padding-bottom: 25px;
                    margin-bottom: 25px;
                }

                h4 {
                    margin-bottom: 25px;
                }

                p {
                    line-height: 30px;
                    margin-bottom: 30px;
                }

                div {
                    display: flex;
                    align-items: center;

                    span:nth-child(2) {
                        margin-left: 10px;
                        margin-right: 10px;
                    }

                    span:nth-child(3) {
                        font-weight: 600;
                        color: $keppel;
                    }
                }
            }

            .right-side-articles {
                display: flex;
                flex-direction: column;

                .top-right-side-article, .bottom-right-side-article {
                    background-color: $dawnPink;
                    display: flex;
                    flex-direction: column;
                    align-items: center;
                    text-align: center;
                    padding: 35px 50px;
                    margin: 0 60px;

                    h3 {
                        font-family: none;
                        font-size: 25px;
                        margin-bottom: 15px;
                    }

                    p {
                        color: $scorpion;
                        font-size: 18px;
                        line-height: 30px;
                    }
                }

                .top-right-side-article {
                    position: relative;
                    
                    :before {
                        border:solid 12px transparent;
                        border-left:solid 12px $dawnPink;
                        border-top:solid 12px $dawnPink;
                        bottom:-22px;
                        content:"";
                        height:0;
                        left:44px;
                        position:absolute;
                        transform:skew(0deg);
                        width:0;
                    }
                }

                .bottom-right-side-article {
                    position: relative;

                    :before {
                        border:solid 12px transparent;
                        border-left:solid 12px $dawnPink;
                        border-top:solid 12px $dawnPink;
                        bottom:-22px;
                        content:"";
                        height:0;
                        left:44px;
                        position:absolute;
                        transform:skew(0deg);
                        width:0;
                    }
                }

                .theGuardian, .theGlobeAndMail {
                    margin: 20px 0 20px 60px;
                    display: flex;
                    align-items: center;
                    
                    span:nth-child(2) {
                        color: $scorpion;
                        font-weight: 600;
                        margin-left: 20px;
                        margin-right: 5px;
                    }
                }
            }
        }
      }
</style>