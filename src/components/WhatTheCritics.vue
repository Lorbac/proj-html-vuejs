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
                
            </div>
            <div class="right-side-articles">

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
          
            .left-side-articles {

            }

            .right-side-articles {

            }
        }
      }
</style>