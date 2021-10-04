<template>
  <section id="blog">
        <div class="top-section">
            <div class="text-left-side">
                <h2>Recent Articles</h2>
                <p>READ THE LATEST ENTRIES</p>
            </div>
            <div class="button-right-side">
                All Articles
            </div>
        </div>
        <div class="bottom-section">
            <div class="left-side-articles">
                <img src="../assets/images/20-Tips-800x471.jpg" alt="">
                <h3>20 Creativity Tips</h3>
                <p>By admin | October 24th, 2019 | Categories: <span>Event, Tips & Tricks</span></p>
                <p>Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Donec velit neque, auctor sit amet aliquam vel, ullamcorper sit amet.</p>
            </div>
            <div class="right-side-articles">
                <div class="article">
                    <img src="../assets/images/thumb-13-2x-320x202.jpg" alt="">
                    <h2>What's On Your Booklist?</h2>
                    <p>October 24th, 2019 | 0 Comments</p>
                </div>
                <div class="article">
                    <img src="../assets/images/thumb-08-2x-320x202.jpg" alt="">
                    <h2>Istanbul Travel Guide</h2>
                    <p>October 24th, 2019 | 0 Comments</p>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: "Blog"
}
</script>

<style lang="scss" scoped>

    @import '../styles/vars.scss';

    #blog {
        background-color: $dawnPink;
        
        .top-section {
            margin: 0 auto;
            width: 70%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: 100px;
            margin-bottom: 60px;
            padding-top: 150px;

            .text-left-side {

                h2 {
                    font-family: none;
                    font-size: 45px;
                    margin-bottom: 20px;
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
                padding: 15px 100px;
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
            justify-content: space-between;
            width: 70%;
            margin: 0px auto;
            padding-bottom: 100px;

            .left-side-articles {
                background-color: $white;
                flex-basis: calc((100% / 3)* 2 - 20px);
                margin-right: 20px;
                
                img {
                    padding: 50px;
                    width: 100%;
                }

                h3 {
                    font-weight: lighter;
                    font-size: 25px;
                    margin-left: 60px;
                }

                p:nth-child(3) {
                    font-size: 14px;

                    span {
                        color: black;
                    }
                }

                p {
                    margin: 10px 0 30px 60px;
                    line-height: 25px;
                    color: $scorpion;
                }
            }

            .right-side-articles {
                flex-basis: calc((100% / 3)* 1 - 20px);
                display: flex;
                flex-direction: column;
                margin-left: 20px;
                background-color: $white;

                .article {

                    img {
                        width: 100%;
                        padding: 30px 30px 10px 30px ;
                    }

                    h2 {
                        padding-left: 30px;
                        font-weight: lighter;
                    }

                    p {
                        padding-left: 30px;
                        font-size: 13px;
                        color: $scorpion;
                        margin: 10px 0;
                    }
                }
                

            }
        }
    }
</style>